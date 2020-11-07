---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
ms.openlocfilehash: b0bebe0f831cc4041ecdeeeaa3ec8066faeacc8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710478"
---
# <span data-ttu-id="3db86-101">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="3db86-101">Set-AzAutomationAccount</span></span>

## <span data-ttu-id="3db86-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3db86-102">SYNOPSIS</span></span>
<span data-ttu-id="3db86-103">Modyfikuje konto usługi Automation.</span><span class="sxs-lookup"><span data-stu-id="3db86-103">Modifies an Automation account.</span></span>

## <span data-ttu-id="3db86-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3db86-104">SYNTAX</span></span>

```
Set-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>] [-Tags <IDictionary>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3db86-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3db86-105">DESCRIPTION</span></span>
<span data-ttu-id="3db86-106">Polecenie cmdlet **Set-AzAutomationAccount** modyfikuje konto usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="3db86-106">The **Set-AzAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>
<span data-ttu-id="3db86-107">Aby uzyskać więcej informacji na temat kont automatyzacji, zobacz polecenie cmdlet New-AzAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="3db86-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="3db86-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3db86-108">EXAMPLES</span></span>

### <span data-ttu-id="3db86-109">Przykład 1. Ustawianie tagów dla konta usługi Automation</span><span class="sxs-lookup"><span data-stu-id="3db86-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="3db86-110">Pierwsze polecenie powoduje przypisanie dwóch par kluczy/wartości zmiennej $Tags.</span><span class="sxs-lookup"><span data-stu-id="3db86-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="3db86-111">Drugie polecenie ustawia znaczniki w $Tags dla konta usługi Automation o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="3db86-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="3db86-112">Przykład 2: Zmienianie planu dla konta usługi Automation</span><span class="sxs-lookup"><span data-stu-id="3db86-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="3db86-113">To polecenie zmienia plan na podstawowy dla konta usługi Automation o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="3db86-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="3db86-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3db86-114">PARAMETERS</span></span>

### <span data-ttu-id="3db86-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3db86-115">-DefaultProfile</span></span>
<span data-ttu-id="3db86-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3db86-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3db86-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3db86-117">-Name</span></span>
<span data-ttu-id="3db86-118">Określa nazwę konta automatyzacji, które jest modyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3db86-118">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3db86-119">-Plan</span><span class="sxs-lookup"><span data-stu-id="3db86-119">-Plan</span></span>
<span data-ttu-id="3db86-120">Określa plan konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="3db86-120">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="3db86-121">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="3db86-121">Valid values are:</span></span>
- <span data-ttu-id="3db86-122">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="3db86-122">Basic</span></span>
- <span data-ttu-id="3db86-123">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="3db86-123">Free</span></span>

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

### <span data-ttu-id="3db86-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3db86-124">-ResourceGroupName</span></span>
<span data-ttu-id="3db86-125">Określa nazwę grupy zasobów zawierającej konto automatyzacji, które jest modyfikowane przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="3db86-125">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3db86-126">-Tagi</span><span class="sxs-lookup"><span data-stu-id="3db86-126">-Tags</span></span>
<span data-ttu-id="3db86-127">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="3db86-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3db86-128">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="3db86-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3db86-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3db86-129">CommonParameters</span></span>
<span data-ttu-id="3db86-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3db86-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3db86-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3db86-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3db86-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3db86-132">INPUTS</span></span>

### <span data-ttu-id="3db86-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3db86-133">System.String</span></span>

### <span data-ttu-id="3db86-134">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="3db86-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="3db86-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3db86-135">OUTPUTS</span></span>

### <span data-ttu-id="3db86-136">Microsoft. Azure. Commands. Automation. model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="3db86-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="3db86-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3db86-137">NOTES</span></span>

## <span data-ttu-id="3db86-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3db86-138">RELATED LINKS</span></span>

[<span data-ttu-id="3db86-139">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="3db86-139">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="3db86-140">Nowe — AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="3db86-140">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="3db86-141">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="3db86-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)