---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: c328dcbf912b5b907f0e27c902bc7eb3dc31a44e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527125"
---
# <span data-ttu-id="8e428-101">Remove-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e428-101">Remove-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="8e428-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8e428-102">SYNOPSIS</span></span>
<span data-ttu-id="8e428-103">Usuwa konfiguracje DSC z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="8e428-103">Removes DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e428-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8e428-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e428-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8e428-105">DESCRIPTION</span></span>
<span data-ttu-id="8e428-106">Polecenie cmdlet **Remove-AzureRmAutomationDscConfiguration** usuwa konfiguracje konfiguracji pożądanego stanu (DSC) z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="8e428-106">The **Remove-AzureRmAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="8e428-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8e428-107">EXAMPLES</span></span>

## <span data-ttu-id="8e428-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8e428-108">PARAMETERS</span></span>

### <span data-ttu-id="8e428-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8e428-109">-AutomationAccountName</span></span>
<span data-ttu-id="8e428-110">Określa nazwę konta automatyzacji zawierającego konfiguracje DSC, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e428-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e428-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e428-111">-DefaultProfile</span></span>
<span data-ttu-id="8e428-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8e428-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e428-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8e428-113">-Force</span></span>
<span data-ttu-id="8e428-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="8e428-114">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e428-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8e428-115">-Name</span></span>
<span data-ttu-id="8e428-116">Określa nazwę konfiguracji DSC, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e428-116">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e428-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e428-117">-ResourceGroupName</span></span>
<span data-ttu-id="8e428-118">Określa nazwę grupy zasobów, dla której to polecenie cmdlet ma pobierać konfigurację DSC.</span><span class="sxs-lookup"><span data-stu-id="8e428-118">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e428-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8e428-119">-Confirm</span></span>
<span data-ttu-id="8e428-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e428-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e428-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e428-121">-WhatIf</span></span>
<span data-ttu-id="8e428-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e428-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e428-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8e428-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e428-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e428-124">CommonParameters</span></span>
<span data-ttu-id="8e428-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e428-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e428-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e428-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e428-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e428-127">INPUTS</span></span>

### <span data-ttu-id="8e428-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8e428-128">None</span></span>
<span data-ttu-id="8e428-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="8e428-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8e428-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8e428-130">OUTPUTS</span></span>

## <span data-ttu-id="8e428-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8e428-131">NOTES</span></span>

## <span data-ttu-id="8e428-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e428-132">RELATED LINKS</span></span>

[<span data-ttu-id="8e428-133">Eksportowanie — AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e428-133">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="8e428-134">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e428-134">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="8e428-135">Import — AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e428-135">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


