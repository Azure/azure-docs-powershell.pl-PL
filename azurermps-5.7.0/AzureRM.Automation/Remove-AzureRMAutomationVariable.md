---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
ms.openlocfilehash: dea9f62583cca8f3a5ee9ce05b6b7e60e8bf4755
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545807"
---
# <span data-ttu-id="ccbd0-101">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="ccbd0-101">Remove-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="ccbd0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ccbd0-102">SYNOPSIS</span></span>
<span data-ttu-id="ccbd0-103">Usuwa zmienną automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="ccbd0-103">Removes an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccbd0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ccbd0-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ccbd0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ccbd0-105">DESCRIPTION</span></span>
<span data-ttu-id="ccbd0-106">Polecenie cmdlet **Remove-AzureRmAutomationVariable** usuwa zmienną z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ccbd0-106">The **Remove-AzureRmAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="ccbd0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ccbd0-107">EXAMPLES</span></span>

### <span data-ttu-id="ccbd0-108">Przykład 1. Usuń zmienną</span><span class="sxs-lookup"><span data-stu-id="ccbd0-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ccbd0-109">To polecenie usuwa zmienną o nazwie StringVariable22 na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ccbd0-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="ccbd0-110">To polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="ccbd0-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="ccbd0-111">W związku z tym nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ccbd0-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ccbd0-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ccbd0-112">PARAMETERS</span></span>

### <span data-ttu-id="ccbd0-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ccbd0-113">-AutomationAccountName</span></span>
<span data-ttu-id="ccbd0-114">Określa nazwę konta automatyzacji zawierającego zmienną, którą to polecenie cmdlet usuwa.</span><span class="sxs-lookup"><span data-stu-id="ccbd0-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="ccbd0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccbd0-115">-DefaultProfile</span></span>
<span data-ttu-id="ccbd0-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ccbd0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ccbd0-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ccbd0-117">-Name</span></span>
<span data-ttu-id="ccbd0-118">Określa nazwę zmiennej, którą to polecenie cmdlet usuwa.</span><span class="sxs-lookup"><span data-stu-id="ccbd0-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccbd0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccbd0-119">-ResourceGroupName</span></span>
<span data-ttu-id="ccbd0-120">Określa grupę zasobów, dla której to polecenie cmdlet usuwa zmienną.</span><span class="sxs-lookup"><span data-stu-id="ccbd0-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="ccbd0-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ccbd0-121">-Confirm</span></span>
<span data-ttu-id="ccbd0-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccbd0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccbd0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccbd0-123">-WhatIf</span></span>
<span data-ttu-id="ccbd0-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccbd0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccbd0-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ccbd0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccbd0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccbd0-126">CommonParameters</span></span>
<span data-ttu-id="ccbd0-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccbd0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccbd0-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccbd0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccbd0-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ccbd0-129">INPUTS</span></span>

### <span data-ttu-id="ccbd0-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ccbd0-130">None</span></span>
<span data-ttu-id="ccbd0-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="ccbd0-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ccbd0-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ccbd0-132">OUTPUTS</span></span>

### <span data-ttu-id="ccbd0-133">Microsoft. Azure. Commands. Automation. model. zmienna</span><span class="sxs-lookup"><span data-stu-id="ccbd0-133">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="ccbd0-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ccbd0-134">NOTES</span></span>

## <span data-ttu-id="ccbd0-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ccbd0-135">RELATED LINKS</span></span>

[<span data-ttu-id="ccbd0-136">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="ccbd0-136">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="ccbd0-137">Nowe — AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="ccbd0-137">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="ccbd0-138">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="ccbd0-138">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


