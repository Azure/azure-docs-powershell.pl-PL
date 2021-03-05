---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: 0b2018eecc081f2fcee5da63ed17cc2e01486777
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960113"
---
# Get-AzTemplateSpec

## SYNOPSIS
Pobiera lub wyświetla specyfikacje szablonu

## SKŁADNIA

### ListTemplateSpecsParameterSet (Domyślne)
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetTemplateSpecByNameParameterSet
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetTemplateSpecByIdParameterSet
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
To polecenie cmdlet służy do listy specyfikacji szablonów w grupie subskrypcji/zasobów lub do uzyskania określonej specyfikacji szablonu według nazwy lub identyfikatora. W przypadku uzyskiwania określonej specyfikacji szablonu według nazwy/identyfikatora można opcjonalnie pobrać określoną wersję, określając nazwę wersji za pomocą **parametru -Version.** W **przypadku korzystania z** wersji -Version w ciągu * będą obecne tylko szczegóły określonej *wersji. Wersje* zwróconego obiektu Spec szablonu. Jeśli podczas pobierania specyfikacji szablonu według nazwy/identyfikatora nie określono konkretnej wersji, wszystkie wersje będą obecne w pliku **. Właściwość* Versions zwróconego obiektu.

**Uwaga:** gdy podano wszystkie specyfikacje szablonów w ramach subskrypcji lub grupy zasobów, każda zwrócona specyfikacja szablonu jest *". Właściwość Versions"* będzie mieć wartość *null.* Informacje o wersji są uwzględniane tylko wtedy, gdy zostaną podane parametry -Name lub -ResourceId (np.: żądasz określonej specyfikacji/wersji szablonu).

## PRZYKŁADY

### Przykład 1. Specyfikacja szablonu listy w bieżącej subskrypcji
```powershell
PS C:\> Get-AzTemplateSpec
```

Zawiera listę wszystkich specyfikacji szablonów w bieżącej subskrypcji.

### Przykład 2. Specyfikacja szablonu listy w grupie zasobów
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

Wyświetla listę wszystkich specyfikacji szablonów w grupie zasobów "myRG" bieżącej subskrypcji.

### Przykład 3. Uzyskiwanie specyfikacji szablonu (ze wszystkimi wersjami) według nazwy
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

Pobiera informacje o specyfikacji szablonu o nazwie "MyTemplateSpec" w grupie zasobów "myRG".

**Uwaga:** Wszystkie wersje specyfikacji szablonów będą dostępne w "*. Właściwość Versions*" obiektu zwracanego.

### Przykład 4. Uzyskiwanie specyfikacji szablonu (konkretnej wersji) według nazwy
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

Pobiera informacje o wersji "1.0" specyfikacji szablonu o nazwie "MyTemplateSpec" w grupie zasobów "myRG".

**Uwaga:** *". Właściwość Versions"* zwróconego obiektu będzie zawierać tylko określoną żądaną wersję.

### Przykład 5. Uzyskiwanie specyfikacji szablonu (ze wszystkimi wersjami) według identyfikatora zasobu
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

Pobiera informacje o specyfikacji szablonu o nazwie "MyTemplateSpec" w grupie zasobów "myRG" \{ podid \} subskrypcji.

**Uwaga:** Wszystkie wersje specyfikacji szablonów będą dostępne w "*. Właściwość Versions*" obiektu zwracanego.

### Przykład 6. Uzyskiwanie specyfikacji szablonu (określonej wersji) według identyfikatora zasobu
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

Pobiera informacje o wersji "1.0" specyfikacji szablonu o nazwie "MyTemplateSpec" w grupie zasobów "myRG" \{ podid \} subskrypcji.

**Uwaga:** *". Właściwość Versions"* zwróconego obiektu będzie zawierać tylko określoną żądaną wersję.

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Nazwa
Nazwa specyfikacji szablonu.

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: System.String
Parameter Sets: ListTemplateSpecsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
W pełni kwalifikowany identyfikator zasobu specyfikacji szablonu. Przykład: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Wersja
Wersja specyfikacji szablonu.

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet, GetTemplateSpecByIdParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSTemplateSpec

## NOTATKI

## LINKI POKREWNE
