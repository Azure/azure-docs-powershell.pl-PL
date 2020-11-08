---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscConfiguration.md
ms.openlocfilehash: bd418037f29aefc27d92ccebe1f34024728c77c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053900"
---
# <span data-ttu-id="5a2f6-101">Remove-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a2f6-101">Remove-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="5a2f6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5a2f6-102">SYNOPSIS</span></span>
<span data-ttu-id="5a2f6-103">Usuwa konfiguracje DSC z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="5a2f6-103">Removes DSC configurations from Automation.</span></span>

## <span data-ttu-id="5a2f6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5a2f6-104">SYNTAX</span></span>

```
Remove-AzAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5a2f6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5a2f6-105">DESCRIPTION</span></span>
<span data-ttu-id="5a2f6-106">Polecenie cmdlet **Remove-AzAutomationDscConfiguration** usuwa konfiguracje konfiguracji pożądanego stanu (DSC) z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="5a2f6-106">The **Remove-AzAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="5a2f6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5a2f6-107">EXAMPLES</span></span>

## <span data-ttu-id="5a2f6-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5a2f6-108">PARAMETERS</span></span>

### <span data-ttu-id="5a2f6-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5a2f6-109">-AutomationAccountName</span></span>
<span data-ttu-id="5a2f6-110">Określa nazwę konta automatyzacji zawierającego konfiguracje DSC, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a2f6-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5a2f6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a2f6-111">-DefaultProfile</span></span>
<span data-ttu-id="5a2f6-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5a2f6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a2f6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5a2f6-113">-Force</span></span>
<span data-ttu-id="5a2f6-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="5a2f6-114">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a2f6-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5a2f6-115">-Name</span></span>
<span data-ttu-id="5a2f6-116">Określa nazwę konfiguracji DSC, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a2f6-116">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a2f6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a2f6-117">-ResourceGroupName</span></span>
<span data-ttu-id="5a2f6-118">Określa nazwę grupy zasobów, dla której to polecenie cmdlet ma pobierać konfigurację DSC.</span><span class="sxs-lookup"><span data-stu-id="5a2f6-118">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="5a2f6-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5a2f6-119">-Confirm</span></span>
<span data-ttu-id="5a2f6-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a2f6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a2f6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a2f6-121">-WhatIf</span></span>
<span data-ttu-id="5a2f6-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a2f6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a2f6-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5a2f6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a2f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a2f6-124">CommonParameters</span></span>
<span data-ttu-id="5a2f6-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a2f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a2f6-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a2f6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a2f6-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a2f6-127">INPUTS</span></span>

### <span data-ttu-id="5a2f6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5a2f6-128">System.String</span></span>

## <span data-ttu-id="5a2f6-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5a2f6-129">OUTPUTS</span></span>

### <span data-ttu-id="5a2f6-130">System. void</span><span class="sxs-lookup"><span data-stu-id="5a2f6-130">System.Void</span></span>

## <span data-ttu-id="5a2f6-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5a2f6-131">NOTES</span></span>

## <span data-ttu-id="5a2f6-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a2f6-132">RELATED LINKS</span></span>

[<span data-ttu-id="5a2f6-133">Eksportowanie — AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a2f6-133">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="5a2f6-134">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a2f6-134">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="5a2f6-135">Import — AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a2f6-135">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


