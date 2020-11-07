---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
ms.openlocfilehash: b336104fea097b0f5adf0993853dd6fff7bba1f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717653"
---
# <span data-ttu-id="bf79a-101">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="bf79a-101">Remove-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="bf79a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bf79a-102">SYNOPSIS</span></span>
<span data-ttu-id="bf79a-103">Usuwa zmienną automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="bf79a-103">Removes an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf79a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bf79a-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bf79a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bf79a-105">DESCRIPTION</span></span>
<span data-ttu-id="bf79a-106">Polecenie cmdlet **Remove-AzureRmAutomationVariable** usuwa zmienną z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="bf79a-106">The **Remove-AzureRmAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="bf79a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bf79a-107">EXAMPLES</span></span>

### <span data-ttu-id="bf79a-108">Przykład 1. Usuń zmienną</span><span class="sxs-lookup"><span data-stu-id="bf79a-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="bf79a-109">To polecenie usuwa zmienną o nazwie StringVariable22 na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="bf79a-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="bf79a-110">To polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="bf79a-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="bf79a-111">W związku z tym nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bf79a-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="bf79a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bf79a-112">PARAMETERS</span></span>

### <span data-ttu-id="bf79a-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bf79a-113">-AutomationAccountName</span></span>
<span data-ttu-id="bf79a-114">Określa nazwę konta automatyzacji zawierającego zmienną, którą to polecenie cmdlet usuwa.</span><span class="sxs-lookup"><span data-stu-id="bf79a-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="bf79a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf79a-115">-DefaultProfile</span></span>
<span data-ttu-id="bf79a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="bf79a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf79a-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bf79a-117">-Name</span></span>
<span data-ttu-id="bf79a-118">Określa nazwę zmiennej, którą to polecenie cmdlet usuwa.</span><span class="sxs-lookup"><span data-stu-id="bf79a-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf79a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf79a-119">-ResourceGroupName</span></span>
<span data-ttu-id="bf79a-120">Określa grupę zasobów, dla której to polecenie cmdlet usuwa zmienną.</span><span class="sxs-lookup"><span data-stu-id="bf79a-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="bf79a-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bf79a-121">-Confirm</span></span>
<span data-ttu-id="bf79a-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf79a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf79a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf79a-123">-WhatIf</span></span>
<span data-ttu-id="bf79a-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf79a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf79a-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bf79a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf79a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf79a-126">CommonParameters</span></span>
<span data-ttu-id="bf79a-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf79a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf79a-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf79a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf79a-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf79a-129">INPUTS</span></span>

### <span data-ttu-id="bf79a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bf79a-130">System.String</span></span>

## <span data-ttu-id="bf79a-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bf79a-131">OUTPUTS</span></span>

### <span data-ttu-id="bf79a-132">System. void</span><span class="sxs-lookup"><span data-stu-id="bf79a-132">System.Void</span></span>

## <span data-ttu-id="bf79a-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bf79a-133">NOTES</span></span>

## <span data-ttu-id="bf79a-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf79a-134">RELATED LINKS</span></span>

[<span data-ttu-id="bf79a-135">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="bf79a-135">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="bf79a-136">Nowe — AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="bf79a-136">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="bf79a-137">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="bf79a-137">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


