.. highlightlang:: c


*************
Pycairo C API
*************

.. currentmodule:: cairo

This manual documents the API used by C and C++ programmers who want to write
extension modules that use pycairo.


.. _api-includes:

To access the Pycairo C API
===========================
Edit the client module file to add the following lines::

  /* All function, type and macro definitions needed to use the Pycairo/C API
   * are included in your code by the following line
   */
  #include "Pycairo.h"

  /* define a variable for the C API */
  static Pycairo_CAPI_t *Pycairo_CAPI;

  /* import pycairo - add to the init<module> function */
  Pycairo_IMPORT;


Pycairo Objects
===============
Objects::

  PycairoContext
  PycairoFontFace
  PycairoToyFontFace
  PycairoFontOptions
  PycairoMatrix
  PycairoPath
  PycairoPattern
  PycairoSolidPattern
  PycairoSurfacePattern
  PycairoGradient
  PycairoLinearGradient
  PycairoRadialGradient
  PycairoScaledFont
  PycairoSurface
  PycairoImageSurface
  PycairoPDFSurface
  PycairoPSSurface
  PycairoSVGSurface
  PycairoWin32Surface
  PycairoXlibSurface


Pycairo Types
=============
Types::

  PyTypeObject *Context_Type;
  PyTypeObject *FontFace_Type;
  PyTypeObject *ToyFontFace_Type;
  PyTypeObject *FontOptions_Type;
  PyTypeObject *Matrix_Type;
  PyTypeObject *Path_Type;
  PyTypeObject *Pattern_Type;
  PyTypeObject *SolidPattern_Type;
  PyTypeObject *SurfacePattern_Type;
  PyTypeObject *Gradient_Type;
  PyTypeObject *LinearGradient_Type;
  PyTypeObject *RadialGradient_Type;
  PyTypeObject *ScaledFont_Type;
  PyTypeObject *Surface_Type;
  PyTypeObject *ImageSurface_Type;
  PyTypeObject *PDFSurface_Type;
  PyTypeObject *PSSurface_Type;
  PyTypeObject *SVGSurface_Type;
  PyTypeObject *Win32Surface_Type;
  PyTypeObject *XlibSurface_Type;


Functions
=========

.. cfunction::  cairo_t * PycairoContext_GET(obj)

   get the C cairo_t * object out of the PycairoContext *obj


.. cfunction::  PyObject * PycairoContext_FromContext(cairo_t *ctx, PyTypeObject *type, PyObject *base)


.. cfunction::  PyObject * PycairoFontFace_FromFontFace(cairo_font_face_t *font_face)


.. cfunction::  PyObject * PycairoFontOptions_FromFontOptions(cairo_font_options_t *font_options)


.. cfunction::  PyObject * PycairoMatrix_FromMatrix(const cairo_matrix_t *matrix)


.. cfunction::  PyObject * PycairoPath_FromPath(cairo_path_t *path)


.. cfunction::  PyObject * PycairoPattern_FromPattern(cairo_pattern_t *pattern, PyObject *base)


.. cfunction::  PyObject * PycairoScaledFont_FromScaledFont(cairo_scaled_font_t *scaled_font)


.. cfunction::  PyObject * PycairoSurface_FromSurface(cairo_surface_t *surface, PyObject *base)


.. cfunction::  int PycairoCheck_Status(cairo_status_t status)
