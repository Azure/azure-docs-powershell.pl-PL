---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
ms.openlocfilehash: bc810da3cd43a18506160d03e6c172eb272bd797
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009834"
---
# <span data-ttu-id="40166-101">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="40166-101">Set-AzAutomationAccount</span></span>

## <span data-ttu-id="40166-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40166-102">SYNOPSIS</span></span>
<span data-ttu-id="40166-103">Modyfikuje konto automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="40166-103">Modifies an Automation account.</span></span>

## <span data-ttu-id="40166-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="40166-104">SYNTAX</span></span>

```
Set-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>] [-Tags <IDictionary>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40166-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="40166-105">DESCRIPTION</span></span>
<span data-ttu-id="40166-106">Polecenie **cmdlet Set-AzAutomationAccount** modyfikuje konto usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="40166-106">The **Set-AzAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>
<span data-ttu-id="40166-107">Aby uzyskać więcej informacji na temat kont automatyzacji, zobacz New-AzAutomationAccount cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40166-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="40166-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="40166-108">EXAMPLES</span></span>

### <span data-ttu-id="40166-109">Przykład 1. Ustawianie tagów dla konta automatyzacji</span><span class="sxs-lookup"><span data-stu-id="40166-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="40166-110">Pierwsze polecenie przypisuje dwie pary klucz/wartość do zmiennej $Tags zmienną.</span><span class="sxs-lookup"><span data-stu-id="40166-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="40166-111">Drugie polecenie ustawia tagi dla $Tags Automatyzacja o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="40166-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="40166-112">Przykład 2. Zmienianie planu dla konta automatyzacji</span><span class="sxs-lookup"><span data-stu-id="40166-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="40166-113">To polecenie zmienia plan na Podstawowy dla konta automatyzacji o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="40166-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="40166-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40166-114">PARAMETERS</span></span>

### <span data-ttu-id="40166-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40166-115">-DefaultProfile</span></span>
<span data-ttu-id="40166-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="40166-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40166-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="40166-117">-Name</span></span>
<span data-ttu-id="40166-118">Określa nazwę konta automatyzacji, które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40166-118">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40166-119">— planowanie</span><span class="sxs-lookup"><span data-stu-id="40166-119">-Plan</span></span>
<span data-ttu-id="40166-120">Określa plan dla konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="40166-120">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="40166-121">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="40166-121">Valid values are:</span></span>
- <span data-ttu-id="40166-122">Podstawowe</span><span class="sxs-lookup"><span data-stu-id="40166-122">Basic</span></span>
- <span data-ttu-id="40166-123">Bezpłatne</span><span class="sxs-lookup"><span data-stu-id="40166-123">Free</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40166-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40166-124">-ResourceGroupName</span></span>
<span data-ttu-id="40166-125">Określa nazwę grupy zasobów zawierającej konto automatyzacji, które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40166-125">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="40166-126">— Tagi</span><span class="sxs-lookup"><span data-stu-id="40166-126">-Tags</span></span>
<span data-ttu-id="40166-127">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="40166-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="40166-128">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="40166-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40166-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40166-129">CommonParameters</span></span>
<span data-ttu-id="40166-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40166-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40166-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40166-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40166-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40166-132">INPUTS</span></span>

### <span data-ttu-id="40166-133">System.String</span><span class="sxs-lookup"><span data-stu-id="40166-133">System.String</span></span>

### <span data-ttu-id="40166-134">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="40166-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="40166-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40166-135">OUTPUTS</span></span>

### <span data-ttu-id="40166-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="40166-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="40166-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="40166-137">NOTES</span></span>

## <span data-ttu-id="40166-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40166-138">RELATED LINKS</span></span>

[<span data-ttu-id="40166-139">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="40166-139">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="40166-140">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="40166-140">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="40166-141">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="40166-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)
