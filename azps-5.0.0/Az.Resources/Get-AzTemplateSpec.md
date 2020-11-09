---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308826"
---
# Get-AzTemplateSpec

## STRESZCZENIe
Pobiera lub wyświetla specyfikacje szablonu

## POLECENIA

### ListTemplateSpecsParameterSet (domyślny)
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

## Opis
Za pomocą tego polecenia cmdlet można wyświetlić specyfikacje szablonu w grupie abonament/zasób lub uzyskać określoną specyfikację szablonu według nazwy lub identyfikatora. Podczas pobierania specyfikacji szablonu według nazwy/identyfikatora można opcjonalnie pobrać określoną wersję przez określenie nazwy wersji za pomocą parametru **-Version** . Gdy używana jest **wersja** , w programie * będą dostępne tylko szczegółowe informacje o wersji *. Wersje* w zwróconym obiekcie specyfikacji szablonu. Jeśli nie określono żadnej konkretnej wersji podczas pobierania specyfikacji szablonu za pomocą nazwy/identyfikatora, wszystkie wersje będą obecne w przeciągu * *. Właściwość wersje* zwracanego obiektu.

**Uwaga** : w przypadku wymieniania wszystkich specyfikacji szablonu w ramach abonamentu lub grupy zasobów każda zwracana Specyfikacja szablonu *". Wersje "* właściwość będzie *wartością null*. Informacje o wersji są dołączane tylko wtedy, gdy są podane parametry Name lub ResourceId (przykład: żądasz konkretnej specyfikacji/wersji szablonu).

## Przykłady

### Przykład 1: Specyfikacja szablonu listy w bieżącym abonamentzie
```powershell
PS C:\> Get-AzTemplateSpec
```

Lista wszystkich specyfikacji szablonu w bieżącej subskrypcji.

### Przykład 2: specyfikacje szablonu listy w grupie zasobów
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

Zawiera wszystkie specyfikacje szablonu w grupie zasobów "myRG" bieżącej subskrypcji.

### Przykład 3: uzyskiwanie specyfikacji szablonu (ze wszystkimi wersjami) według nazwy
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

Pobiera informacje o specyfikacji szablonu o nazwie "MyTemplateSpec" w grupie zasobów "myRG".

**Uwaga** : wszystkie wersje specyfikacji szablonu będą obecne w ramach " *.* Właściwość (wersje) obiektu zwracanego.

### Przykład 4: uzyskiwanie specyfikacji szablonu (określonej wersji) według nazwy
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

Pobiera informacje o wersji "v 1.0" specyfikacji szablonu o nazwie "MyTemplateSpec" w grupie zasobów "myRG".

**Uwaga** : *". Właściwość wersje "* zwróconego obiektu" będzie zawierać tylko żądaną wersję.

### Przykład 5: uzyskiwanie specyfikacji szablonu (ze wszystkimi wersjami) według identyfikatora zasobu
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

Pobiera informacje o specyfikacji szablonu o nazwie "MyTemplateSpec" w grupie zasobów "myRG" subskrypcji \{ subId \} .

**Uwaga** : wszystkie wersje specyfikacji szablonu będą obecne w ramach " *.* Właściwość (wersje) obiektu zwracanego.

### Przykład 6: uzyskiwanie specyfikacji szablonu (określonej wersji) według identyfikatora zasobu
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

Pobiera informacje o wersji "v 1.0" specyfikacji szablonu o nazwie "MyTemplateSpec" w grupie zasobów "myRG" subskrypcji \{ subId \} .

**Uwaga** : *". Właściwość wersje "* zwróconego obiektu" będzie zawierać tylko żądaną wersję.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -Name (nazwa)
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
W pełni kwalifikowany identyfikator zasobu specyfikacji szablonu. przykład:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}

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

### -Version
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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSTemplateSpec

## INFORMACYJN

## LINKI POKREWNE
