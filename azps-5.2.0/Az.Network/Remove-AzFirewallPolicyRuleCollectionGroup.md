---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 3c9b307b34d07ff6c9331dc8d72c1149c83ef374
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363526"
---
# <span data-ttu-id="fe00e-101">Remove-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="fe00e-101">Remove-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="fe00e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fe00e-102">SYNOPSIS</span></span>
<span data-ttu-id="fe00e-103">Usuwa grupę kolekcji reguł zasad zapory platformy Azure w zasadach zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="fe00e-103">Removes a Azure Firewall Policy Rule Collection Group in a Azure firewall policy</span></span>

## <span data-ttu-id="fe00e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fe00e-104">SYNTAX</span></span>

### <span data-ttu-id="fe00e-105">RemoveByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fe00e-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe00e-106">RemoveByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe00e-106">RemoveByParentInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe00e-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe00e-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe00e-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe00e-108">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe00e-109">Opis</span><span class="sxs-lookup"><span data-stu-id="fe00e-109">DESCRIPTION</span></span>
<span data-ttu-id="fe00e-110">Polecenie cmdlet **Remove-AzFirewallPolicyRuleCollectionGroup** usuwa grupę kolekcji reguł z zasad zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fe00e-110">The **Remove-AzFirewallPolicyRuleCollectionGroup** cmdlet removes a rule collection group from an Azure Firewall Policy.</span></span>

## <span data-ttu-id="fe00e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fe00e-111">EXAMPLES</span></span>

### <span data-ttu-id="fe00e-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fe00e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -FirewallPolicyObject $fp
```

<span data-ttu-id="fe00e-113">W tym przykładzie jest usuwana colelctiona reguła zasad zapory o nazwie "testRcGroup" w obiekcie zasad zapory $fp</span><span class="sxs-lookup"><span data-stu-id="fe00e-113">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall policy object $fp</span></span>

### <span data-ttu-id="fe00e-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fe00e-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -ResourceGroupName testRg -AzureFirewallPolicyName fpName 
```

<span data-ttu-id="fe00e-115">W tym przykładzie jest usuwana colelctiona reguła zasad zapory o nazwie "testRcGroup" w zaporze o nazwie "fpName" frpm nazw "testRg".</span><span class="sxs-lookup"><span data-stu-id="fe00e-115">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall named "fpName" frpm the resourcegroup names "testRg"</span></span>

## <span data-ttu-id="fe00e-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe00e-116">PARAMETERS</span></span>

### <span data-ttu-id="fe00e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe00e-117">-AsJob</span></span>
<span data-ttu-id="fe00e-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fe00e-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe00e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe00e-119">-DefaultProfile</span></span>
<span data-ttu-id="fe00e-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe00e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe00e-121">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="fe00e-121">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="fe00e-122">Nazwa zasad zapory</span><span class="sxs-lookup"><span data-stu-id="fe00e-122">The name of the firewall policy</span></span>

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

### <span data-ttu-id="fe00e-123">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="fe00e-123">-FirewallPolicyObject</span></span>
<span data-ttu-id="fe00e-124">Zasady zapory.</span><span class="sxs-lookup"><span data-stu-id="fe00e-124">Firewall Policy.</span></span>

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

### <span data-ttu-id="fe00e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="fe00e-125">-Force</span></span>
<span data-ttu-id="fe00e-126">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fe00e-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fe00e-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fe00e-127">-InputObject</span></span>
<span data-ttu-id="fe00e-128">Obiekt grupy kolekcji reguł zasad zapory</span><span class="sxs-lookup"><span data-stu-id="fe00e-128">Firewall Policy Rule collection group object</span></span>

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

### <span data-ttu-id="fe00e-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fe00e-129">-Name</span></span>
<span data-ttu-id="fe00e-130">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="fe00e-130">The resource name.</span></span>

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

### <span data-ttu-id="fe00e-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe00e-131">-PassThru</span></span>
<span data-ttu-id="fe00e-132">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="fe00e-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fe00e-133">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="fe00e-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fe00e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe00e-134">-ResourceGroupName</span></span>
<span data-ttu-id="fe00e-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fe00e-135">The resource group name.</span></span>

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

### <span data-ttu-id="fe00e-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe00e-136">-ResourceId</span></span>
<span data-ttu-id="fe00e-137">Identyfikator zasobu grupy kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="fe00e-137">The resource Id of the Rule collection groupy</span></span>

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

### <span data-ttu-id="fe00e-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fe00e-138">-Confirm</span></span>
<span data-ttu-id="fe00e-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe00e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe00e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe00e-140">-WhatIf</span></span>
<span data-ttu-id="fe00e-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe00e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe00e-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fe00e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe00e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe00e-143">CommonParameters</span></span>
<span data-ttu-id="fe00e-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe00e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe00e-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe00e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe00e-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe00e-146">INPUTS</span></span>

### <span data-ttu-id="fe00e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="fe00e-147">System.String</span></span>

### <span data-ttu-id="fe00e-148">Microsoft. Azure. Commands. Network. models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="fe00e-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="fe00e-149">Microsoft. Azure. Commands. Network. models. PSAzureFirewallPolicyRuleCollectionGroupWrapper</span><span class="sxs-lookup"><span data-stu-id="fe00e-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span></span>

## <span data-ttu-id="fe00e-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fe00e-150">OUTPUTS</span></span>

### <span data-ttu-id="fe00e-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fe00e-151">System.Boolean</span></span>

## <span data-ttu-id="fe00e-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fe00e-152">NOTES</span></span>

## <span data-ttu-id="fe00e-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe00e-153">RELATED LINKS</span></span>
