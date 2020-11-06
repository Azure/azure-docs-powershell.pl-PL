---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
ms.openlocfilehash: 8ad63c37c366c0f9c7693585f3a3c2fd57de4fdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528317"
---
# <span data-ttu-id="fae6c-101">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="fae6c-101">Set-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="fae6c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fae6c-102">SYNOPSIS</span></span>
<span data-ttu-id="fae6c-103">Modyfikuje konto usługi Automation.</span><span class="sxs-lookup"><span data-stu-id="fae6c-103">Modifies an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fae6c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fae6c-104">SYNTAX</span></span>

```
Set-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fae6c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fae6c-105">DESCRIPTION</span></span>
<span data-ttu-id="fae6c-106">Polecenie cmdlet **Set-AzureRmAutomationAccount** modyfikuje konto usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="fae6c-106">The **Set-AzureRmAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>

<span data-ttu-id="fae6c-107">Aby uzyskać więcej informacji na temat kont automatyzacji, zobacz polecenie cmdlet New-AzureRmAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="fae6c-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="fae6c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fae6c-108">EXAMPLES</span></span>

### <span data-ttu-id="fae6c-109">Przykład 1. Ustawianie tagów dla konta usługi Automation</span><span class="sxs-lookup"><span data-stu-id="fae6c-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="fae6c-110">Pierwsze polecenie powoduje przypisanie dwóch par kluczy/wartości zmiennej $Tags.</span><span class="sxs-lookup"><span data-stu-id="fae6c-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="fae6c-111">Drugie polecenie ustawia znaczniki w $Tags dla konta usługi Automation o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="fae6c-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="fae6c-112">Przykład 2: Zmienianie planu dla konta usługi Automation</span><span class="sxs-lookup"><span data-stu-id="fae6c-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="fae6c-113">To polecenie zmienia plan na podstawowy dla konta usługi Automation o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="fae6c-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="fae6c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fae6c-114">PARAMETERS</span></span>

### <span data-ttu-id="fae6c-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fae6c-115">-Name</span></span>
<span data-ttu-id="fae6c-116">Określa nazwę konta automatyzacji, które jest modyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fae6c-116">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="fae6c-117">-Plan</span><span class="sxs-lookup"><span data-stu-id="fae6c-117">-Plan</span></span>
<span data-ttu-id="fae6c-118">Określa plan konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="fae6c-118">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="fae6c-119">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="fae6c-119">Valid values are:</span></span>

- <span data-ttu-id="fae6c-120">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="fae6c-120">Basic</span></span>
- <span data-ttu-id="fae6c-121">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="fae6c-121">Free</span></span>

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

### <span data-ttu-id="fae6c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fae6c-122">-ResourceGroupName</span></span>
<span data-ttu-id="fae6c-123">Określa nazwę grupy zasobów zawierającej konto automatyzacji, które jest modyfikowane przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="fae6c-123">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="fae6c-124">-Tagi</span><span class="sxs-lookup"><span data-stu-id="fae6c-124">-Tags</span></span>
<span data-ttu-id="fae6c-125">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="fae6c-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fae6c-126">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="fae6c-126">For example:</span></span>

<span data-ttu-id="fae6c-127">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="fae6c-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fae6c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fae6c-128">-DefaultProfile</span></span>
<span data-ttu-id="fae6c-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fae6c-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fae6c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fae6c-130">CommonParameters</span></span>
<span data-ttu-id="fae6c-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fae6c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fae6c-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fae6c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fae6c-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fae6c-133">INPUTS</span></span>

## <span data-ttu-id="fae6c-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fae6c-134">OUTPUTS</span></span>

### <span data-ttu-id="fae6c-135">Microsoft. Azure. Commands. Automation. model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="fae6c-135">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="fae6c-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fae6c-136">NOTES</span></span>

## <span data-ttu-id="fae6c-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fae6c-137">RELATED LINKS</span></span>

[<span data-ttu-id="fae6c-138">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="fae6c-138">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="fae6c-139">Nowe — AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="fae6c-139">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="fae6c-140">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="fae6c-140">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)
