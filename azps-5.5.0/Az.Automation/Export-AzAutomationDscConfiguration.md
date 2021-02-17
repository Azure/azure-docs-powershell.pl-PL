---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
ms.openlocfilehash: 27fbac9c368725a25845454adf044c2ff6704f3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197123"
---
# <span data-ttu-id="9225b-101">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9225b-101">Export-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="9225b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9225b-102">SYNOPSIS</span></span>
<span data-ttu-id="9225b-103">Eksportuje konfigurację dsC z automatyzacji do pliku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="9225b-103">Exports a DSC configuration from Automation to a local file.</span></span>

## <span data-ttu-id="9225b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9225b-104">SYNTAX</span></span>

```
Export-AzAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9225b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9225b-105">DESCRIPTION</span></span>
<span data-ttu-id="9225b-106">Polecenie **cmdlet Export-AzAutomationDscConfiguration** eksportuje konfigurację APS Desired State Configuration (DSC) z automatyzacji azure do pliku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="9225b-106">The **Export-AzAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="9225b-107">Wyeksportowany plik ma rozszerzenie nazwy pliku ps1.</span><span class="sxs-lookup"><span data-stu-id="9225b-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="9225b-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9225b-108">EXAMPLES</span></span>

### <span data-ttu-id="9225b-109">Przykład 1. Eksportowanie opublikowanej wersji konfiguracji dsc</span><span class="sxs-lookup"><span data-stu-id="9225b-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="9225b-110">To polecenie eksportuje opublikowaną wersję konfiguracji dsc w automatyzacji do określonego folderu, który jest pulpitem.</span><span class="sxs-lookup"><span data-stu-id="9225b-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="9225b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9225b-111">PARAMETERS</span></span>

### <span data-ttu-id="9225b-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9225b-112">-AutomationAccountName</span></span>
<span data-ttu-id="9225b-113">Określa nazwę konta automatyzacji zawierającego zestaw danych DSC eksportowanych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9225b-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9225b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9225b-114">-DefaultProfile</span></span>
<span data-ttu-id="9225b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="9225b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9225b-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="9225b-116">-Force</span></span>
<span data-ttu-id="9225b-117">Wskazuje, że to polecenie cmdlet zastępuje istniejący plik lokalny nowym plikiem o tej samej nazwie.</span><span class="sxs-lookup"><span data-stu-id="9225b-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9225b-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9225b-118">-Name</span></span>
<span data-ttu-id="9225b-119">Określa nazwę konfiguracji dsc eksportowanych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9225b-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9225b-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="9225b-120">-OutputFolder</span></span>
<span data-ttu-id="9225b-121">Określa folder wyjściowy, do którego to polecenie cmdlet eksportuje konfigurację DSC.</span><span class="sxs-lookup"><span data-stu-id="9225b-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9225b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9225b-122">-ResourceGroupName</span></span>
<span data-ttu-id="9225b-123">Określa nazwę grupy zasobów, dla której to polecenie cmdlet eksportuje konfigurację DSC.</span><span class="sxs-lookup"><span data-stu-id="9225b-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9225b-124">— Slot</span><span class="sxs-lookup"><span data-stu-id="9225b-124">-Slot</span></span>
<span data-ttu-id="9225b-125">Określa, która wersja konfiguracji dsC jest eksportowana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9225b-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="9225b-126">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="9225b-126">Valid values are:</span></span> 
- <span data-ttu-id="9225b-127">Wersja robocza</span><span class="sxs-lookup"><span data-stu-id="9225b-127">Draft</span></span>
- <span data-ttu-id="9225b-128">Published Wartość domyślna to Published.</span><span class="sxs-lookup"><span data-stu-id="9225b-128">Published The default value is Published.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9225b-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9225b-129">-Confirm</span></span>
<span data-ttu-id="9225b-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9225b-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9225b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9225b-131">-WhatIf</span></span>
<span data-ttu-id="9225b-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9225b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9225b-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9225b-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9225b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9225b-134">CommonParameters</span></span>
<span data-ttu-id="9225b-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9225b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9225b-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9225b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9225b-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9225b-137">INPUTS</span></span>

### <span data-ttu-id="9225b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="9225b-138">System.String</span></span>

## <span data-ttu-id="9225b-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9225b-139">OUTPUTS</span></span>

### <span data-ttu-id="9225b-140">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="9225b-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="9225b-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9225b-141">NOTES</span></span>

## <span data-ttu-id="9225b-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9225b-142">RELATED LINKS</span></span>

[<span data-ttu-id="9225b-143">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9225b-143">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="9225b-144">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9225b-144">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


