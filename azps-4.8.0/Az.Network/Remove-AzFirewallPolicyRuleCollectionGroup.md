---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 3c9b307b34d07ff6c9331dc8d72c1149c83ef374
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063911"
---
# <span data-ttu-id="77461-101">Remove-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="77461-101">Remove-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="77461-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77461-102">SYNOPSIS</span></span>
<span data-ttu-id="77461-103">Usuwa grupę kolekcji reguł zasad zapory platformy Azure w zasadach zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="77461-103">Removes a Azure Firewall Policy Rule Collection Group in a Azure firewall policy</span></span>

## <span data-ttu-id="77461-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77461-104">SYNTAX</span></span>

### <span data-ttu-id="77461-105">RemoveByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="77461-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77461-106">RemoveByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77461-106">RemoveByParentInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="77461-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77461-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="77461-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77461-108">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77461-109">Opis</span><span class="sxs-lookup"><span data-stu-id="77461-109">DESCRIPTION</span></span>
<span data-ttu-id="77461-110">Polecenie cmdlet **Remove-AzFirewallPolicyRuleCollectionGroup** usuwa grupę kolekcji reguł z zasad zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="77461-110">The **Remove-AzFirewallPolicyRuleCollectionGroup** cmdlet removes a rule collection group from an Azure Firewall Policy.</span></span>

## <span data-ttu-id="77461-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77461-111">EXAMPLES</span></span>

### <span data-ttu-id="77461-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="77461-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -FirewallPolicyObject $fp
```

<span data-ttu-id="77461-113">W tym przykładzie jest usuwana colelctiona reguła zasad zapory o nazwie "testRcGroup" w obiekcie zasad zapory $fp</span><span class="sxs-lookup"><span data-stu-id="77461-113">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall policy object $fp</span></span>

### <span data-ttu-id="77461-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="77461-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -ResourceGroupName testRg -AzureFirewallPolicyName fpName 
```

<span data-ttu-id="77461-115">W tym przykładzie jest usuwana colelctiona reguła zasad zapory o nazwie "testRcGroup" w zaporze o nazwie "fpName" frpm nazw "testRg".</span><span class="sxs-lookup"><span data-stu-id="77461-115">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall named "fpName" frpm the resourcegroup names "testRg"</span></span>

## <span data-ttu-id="77461-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77461-116">PARAMETERS</span></span>

### <span data-ttu-id="77461-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77461-117">-AsJob</span></span>
<span data-ttu-id="77461-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="77461-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77461-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77461-119">-DefaultProfile</span></span>
<span data-ttu-id="77461-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77461-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77461-121">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="77461-121">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="77461-122">Nazwa zasad zapory</span><span class="sxs-lookup"><span data-stu-id="77461-122">The name of the firewall policy</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77461-123">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="77461-123">-FirewallPolicyObject</span></span>
<span data-ttu-id="77461-124">Zasady zapory.</span><span class="sxs-lookup"><span data-stu-id="77461-124">Firewall Policy.</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: RemoveByParentInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77461-125">-Force</span><span class="sxs-lookup"><span data-stu-id="77461-125">-Force</span></span>
<span data-ttu-id="77461-126">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="77461-126">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77461-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="77461-127">-InputObject</span></span>
<span data-ttu-id="77461-128">Obiekt grupy kolekcji reguł zasad zapory</span><span class="sxs-lookup"><span data-stu-id="77461-128">Firewall Policy Rule collection group object</span></span>

```yaml
Type: PSAzureFirewallPolicyRuleCollectionGroupWrapper
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77461-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="77461-129">-Name</span></span>
<span data-ttu-id="77461-130">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="77461-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: RemoveByParentInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77461-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77461-131">-PassThru</span></span>
<span data-ttu-id="77461-132">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="77461-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="77461-133">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="77461-133">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77461-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77461-134">-ResourceGroupName</span></span>
<span data-ttu-id="77461-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="77461-135">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77461-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77461-136">-ResourceId</span></span>
<span data-ttu-id="77461-137">Identyfikator zasobu grupy kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="77461-137">The resource Id of the Rule collection groupy</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77461-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="77461-138">-Confirm</span></span>
<span data-ttu-id="77461-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77461-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77461-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77461-140">-WhatIf</span></span>
<span data-ttu-id="77461-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77461-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77461-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="77461-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77461-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77461-143">CommonParameters</span></span>
<span data-ttu-id="77461-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77461-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77461-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77461-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77461-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77461-146">INPUTS</span></span>

### <span data-ttu-id="77461-147">System. String</span><span class="sxs-lookup"><span data-stu-id="77461-147">System.String</span></span>

### <span data-ttu-id="77461-148">Microsoft. Azure. Commands. Network. models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="77461-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="77461-149">Microsoft. Azure. Commands. Network. models. PSAzureFirewallPolicyRuleCollectionGroupWrapper</span><span class="sxs-lookup"><span data-stu-id="77461-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span></span>

## <span data-ttu-id="77461-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77461-150">OUTPUTS</span></span>

### <span data-ttu-id="77461-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="77461-151">System.Boolean</span></span>

## <span data-ttu-id="77461-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77461-152">NOTES</span></span>

## <span data-ttu-id="77461-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77461-153">RELATED LINKS</span></span>
