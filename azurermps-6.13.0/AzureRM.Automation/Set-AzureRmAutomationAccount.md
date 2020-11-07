---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
ms.openlocfilehash: 7a0341221dee0f282508377d1233e30deae1fcee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716458"
---
# <span data-ttu-id="0e0bd-101">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="0e0bd-101">Set-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="0e0bd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0e0bd-102">SYNOPSIS</span></span>
<span data-ttu-id="0e0bd-103">Modyfikuje konto usługi Automation.</span><span class="sxs-lookup"><span data-stu-id="0e0bd-103">Modifies an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e0bd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0e0bd-104">SYNTAX</span></span>

```
Set-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e0bd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0e0bd-105">DESCRIPTION</span></span>
<span data-ttu-id="0e0bd-106">Polecenie cmdlet **Set-AzureRmAutomationAccount** modyfikuje konto usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="0e0bd-106">The **Set-AzureRmAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>
<span data-ttu-id="0e0bd-107">Aby uzyskać więcej informacji na temat kont automatyzacji, zobacz polecenie cmdlet New-AzureRmAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="0e0bd-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="0e0bd-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0e0bd-108">EXAMPLES</span></span>

### <span data-ttu-id="0e0bd-109">Przykład 1. Ustawianie tagów dla konta usługi Automation</span><span class="sxs-lookup"><span data-stu-id="0e0bd-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="0e0bd-110">Pierwsze polecenie powoduje przypisanie dwóch par kluczy/wartości zmiennej $Tags.</span><span class="sxs-lookup"><span data-stu-id="0e0bd-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="0e0bd-111">Drugie polecenie ustawia znaczniki w $Tags dla konta usługi Automation o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="0e0bd-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="0e0bd-112">Przykład 2: Zmienianie planu dla konta usługi Automation</span><span class="sxs-lookup"><span data-stu-id="0e0bd-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="0e0bd-113">To polecenie zmienia plan na podstawowy dla konta usługi Automation o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="0e0bd-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="0e0bd-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e0bd-114">PARAMETERS</span></span>

### <span data-ttu-id="0e0bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e0bd-115">-DefaultProfile</span></span>
<span data-ttu-id="0e0bd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0e0bd-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e0bd-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0e0bd-117">-Name</span></span>
<span data-ttu-id="0e0bd-118">Określa nazwę konta automatyzacji, które jest modyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e0bd-118">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0e0bd-119">-Plan</span><span class="sxs-lookup"><span data-stu-id="0e0bd-119">-Plan</span></span>
<span data-ttu-id="0e0bd-120">Określa plan konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="0e0bd-120">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="0e0bd-121">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="0e0bd-121">Valid values are:</span></span>
- <span data-ttu-id="0e0bd-122">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="0e0bd-122">Basic</span></span>
- <span data-ttu-id="0e0bd-123">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="0e0bd-123">Free</span></span>

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

### <span data-ttu-id="0e0bd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e0bd-124">-ResourceGroupName</span></span>
<span data-ttu-id="0e0bd-125">Określa nazwę grupy zasobów zawierającej konto automatyzacji, które jest modyfikowane przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="0e0bd-125">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0e0bd-126">-Tagi</span><span class="sxs-lookup"><span data-stu-id="0e0bd-126">-Tags</span></span>
<span data-ttu-id="0e0bd-127">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="0e0bd-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0e0bd-128">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="0e0bd-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0e0bd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e0bd-129">CommonParameters</span></span>
<span data-ttu-id="0e0bd-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e0bd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e0bd-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e0bd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e0bd-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e0bd-132">INPUTS</span></span>

### <span data-ttu-id="0e0bd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0e0bd-133">System.String</span></span>

### <span data-ttu-id="0e0bd-134">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="0e0bd-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="0e0bd-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0e0bd-135">OUTPUTS</span></span>

### <span data-ttu-id="0e0bd-136">Microsoft. Azure. Commands. Automation. model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="0e0bd-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="0e0bd-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0e0bd-137">NOTES</span></span>

## <span data-ttu-id="0e0bd-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e0bd-138">RELATED LINKS</span></span>

[<span data-ttu-id="0e0bd-139">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="0e0bd-139">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="0e0bd-140">Nowe — AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="0e0bd-140">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="0e0bd-141">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="0e0bd-141">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)
