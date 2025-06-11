# 🔢 Contador Numérico – Proyecto en Visual Basic .NET

Este proyecto es una aplicación de escritorio desarrollada en Visual Basic usando Visual Studio. El programa permite generar una secuencia numérica controlada por el usuario a través de tres parámetros: **valor inicial**, **cantidad de repeticiones** y **valor incremental**.

---

## 🖥️ Captura de pantalla

### Vista inicial:
![Vista inicial](./faf1f0ca-ab54-43aa-810e-fb05d8b4fecb.png)

### Vista con resultado generado:
![Resultado](./7fbb2d3b-739a-403e-873a-6779c55a6a28.png)

---

## 🎯 Objetivo del programa

El usuario introduce tres datos:
- **Valor inicial**: el número desde donde comienza la secuencia.
- **Repeticiones**: cuántos números desea generar.
- **Incremental**: de cuánto en cuánto se aumenta.

Al presionar el botón **“Calcular”**, el programa:
1. Calcula la secuencia.
2. Muestra los valores en un `ListBox`.

---

## 🔧 Tecnologías utilizadas

- Visual Basic .NET
- Visual Studio
- Windows Forms
- Controles: `TextBox`, `ListBox`, `Button`

---

## 💡 Código principal

```vb
Private Sub CalcularBtn_Click(sender As Object, e As EventArgs) Handles CalcularBtn.Click
    Dim i As Integer
    Dim Repeticiones As Integer
    Dim Incremental As Integer
    Dim Indice As Integer

    Indice = RepeticionesTxt.Text - 1
    Dim Valores(Indice) As Integer

    LimpiarListBox()

    Repeticiones = RepeticionesTxt.Text - 1
    Incremental = Val(ValorInicialTxt.Text)

    For i = 0 To Repeticiones
        Valores(i) = Incremental
        Incremental += Val(IncremetalTxt.Text)
    Next i

    AddValues(Valores)
End Sub
