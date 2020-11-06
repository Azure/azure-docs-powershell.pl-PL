---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: ed35cf910dd0bf51803b6a38edc90a93f5411520
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525721"
---
# <span data-ttu-id="9b8ec-101">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b8ec-101">Export-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="9b8ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9b8ec-102">SYNOPSIS</span></span>
<span data-ttu-id="9b8ec-103">Umożliwia wyeksportowanie konfiguracji DSC z automatyzacji do pliku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="9b8ec-103">Exports a DSC configuration from Automation to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b8ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9b8ec-104">SYNTAX</span></span>

```
Export-AzureRmAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b8ec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9b8ec-105">DESCRIPTION</span></span>
<span data-ttu-id="9b8ec-106">Polecenie cmdlet **Export-AzureRmAutomationDscConfiguration** umożliwia wyeksportowanie konfiguracji programu APS (żądana konfiguracja) z usługi Azure Automation do pliku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="9b8ec-106">The **Export-AzureRmAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="9b8ec-107">Wyeksportowany plik ma rozszerzenie nazwy pliku ps1.</span><span class="sxs-lookup"><span data-stu-id="9b8ec-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="9b8ec-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9b8ec-108">EXAMPLES</span></span>

### <span data-ttu-id="9b8ec-109">Przykład 1. Eksportowanie opublikowanej wersji konfiguracji DSC</span><span class="sxs-lookup"><span data-stu-id="9b8ec-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="9b8ec-110">To polecenie eksportuje opublikowaną wersję konfiguracji DSC w aplikacji Automation do określonego folderu, który jest pulpitem.</span><span class="sxs-lookup"><span data-stu-id="9b8ec-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="9b8ec-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9b8ec-111">PARAMETERS</span></span>

### <span data-ttu-id="9b8ec-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9b8ec-112">-AutomationAccountName</span></span>
<span data-ttu-id="9b8ec-113">Określa nazwę konta automatyzacji zawierającego DSC, które jest eksportowane za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b8ec-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="9b8ec-114">-Force</span><span class="sxs-lookup"><span data-stu-id="9b8ec-114">-Force</span></span>
<span data-ttu-id="9b8ec-115">Wskazuje, że to polecenie cmdlet Zamienia istniejący plik lokalny na nowy plik o tej samej nazwie.</span><span class="sxs-lookup"><span data-stu-id="9b8ec-115">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="9b8ec-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9b8ec-116">-Name</span></span>
<span data-ttu-id="9b8ec-117">Określa nazwę konfiguracji DSC wyeksportowanej przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b8ec-117">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

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

### <span data-ttu-id="9b8ec-118">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="9b8ec-118">-OutputFolder</span></span>
<span data-ttu-id="9b8ec-119">Określa folder wyjściowy, w którym ten aplet polecenia wyeksportuje konfigurację DSC.</span><span class="sxs-lookup"><span data-stu-id="9b8ec-119">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="9b8ec-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b8ec-120">-ResourceGroupName</span></span>
<span data-ttu-id="9b8ec-121">Określa nazwę grupy zasobów, dla której to polecenie cmdlet eksportuje konfigurację DSC.</span><span class="sxs-lookup"><span data-stu-id="9b8ec-121">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="9b8ec-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="9b8ec-122">-Slot</span></span>
<span data-ttu-id="9b8ec-123">Określa wersję konfiguracji DSC wyeksportowanej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b8ec-123">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="9b8ec-124">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="9b8ec-124">Valid values are:</span></span> 

- <span data-ttu-id="9b8ec-125">Propozycje</span><span class="sxs-lookup"><span data-stu-id="9b8ec-125">Draft</span></span>
- <span data-ttu-id="9b8ec-126">Podawane</span><span class="sxs-lookup"><span data-stu-id="9b8ec-126">Published</span></span> 

<span data-ttu-id="9b8ec-127">Wartość domyślna jest publikowana.</span><span class="sxs-lookup"><span data-stu-id="9b8ec-127">The default value is Published.</span></span>

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

### <span data-ttu-id="9b8ec-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9b8ec-128">-Confirm</span></span>
<span data-ttu-id="9b8ec-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b8ec-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b8ec-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b8ec-130">-WhatIf</span></span>
<span data-ttu-id="9b8ec-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b8ec-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b8ec-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9b8ec-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b8ec-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b8ec-133">-DefaultProfile</span></span>
<span data-ttu-id="9b8ec-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b8ec-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b8ec-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b8ec-135">CommonParameters</span></span>
<span data-ttu-id="9b8ec-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b8ec-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b8ec-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b8ec-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b8ec-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b8ec-138">INPUTS</span></span>

## <span data-ttu-id="9b8ec-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9b8ec-139">OUTPUTS</span></span>

### <span data-ttu-id="9b8ec-140">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="9b8ec-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="9b8ec-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9b8ec-141">NOTES</span></span>

## <span data-ttu-id="9b8ec-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b8ec-142">RELATED LINKS</span></span>

[<span data-ttu-id="9b8ec-143">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b8ec-143">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="9b8ec-144">Import — AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b8ec-144">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


