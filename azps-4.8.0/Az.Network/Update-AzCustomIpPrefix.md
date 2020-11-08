---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
ms.openlocfilehash: 65d47c57720e66ecad8267ae45f9e08eb3e4c4ca
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223012"
---
# <span data-ttu-id="7e870-101">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7e870-101">Update-AzCustomIpPrefix</span></span>

## <span data-ttu-id="7e870-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7e870-102">SYNOPSIS</span></span>
<span data-ttu-id="7e870-103">Aktualizuje CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7e870-103">Updates a CustomIpPrefix</span></span>

## <span data-ttu-id="7e870-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7e870-104">SYNTAX</span></span>

### <span data-ttu-id="7e870-105">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e870-105">UpdateByNameParameterSet</span></span>
```
Update-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Commission] [-Decomission]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e870-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e870-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Commission] [-Decomission] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e870-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e870-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzCustomIpPrefix -ResourceId <String> [-Commission] [-Decomission] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e870-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7e870-108">DESCRIPTION</span></span>
<span data-ttu-id="7e870-109">Polecenie cmdlet **Update-AzCustomIpPrefix** umożliwia użytkownikowi przeprowadzenie lub zlikwidowanie CustomIpPrefix lub edytowanie tagów zasobu.</span><span class="sxs-lookup"><span data-stu-id="7e870-109">The **Update-AzCustomIpPrefix** cmdlet allows the user to either commission or decommission their CustomIpPrefix, or edit the tags of the resource.</span></span>

## <span data-ttu-id="7e870-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7e870-110">EXAMPLES</span></span>

### <span data-ttu-id="7e870-111">Przykład 1. CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7e870-111">Example 1 : Commission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Commission
```

<span data-ttu-id="7e870-112">Powyższe polecenie rozpocznie proces CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="7e870-112">The above command will start the commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="7e870-113">Przykład 2: Likwidowanie CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7e870-113">Example 2 : Decommission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Decommission
```

<span data-ttu-id="7e870-114">Powyższe polecenie rozpocznie proces likwidacji CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="7e870-114">The above command will start the de-commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="7e870-115">Przykład 3: aktualizowanie znaczników dla CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7e870-115">Example 3 : Update tags for the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Tag $tags
```

<span data-ttu-id="7e870-116">Powyższe polecenie zaktualizuje znaczniki CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="7e870-116">The above command will update the tags for the CustomIpPrefix.</span></span>

## <span data-ttu-id="7e870-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e870-117">PARAMETERS</span></span>

### <span data-ttu-id="7e870-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e870-118">-AsJob</span></span>
<span data-ttu-id="7e870-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7e870-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e870-120">-Prowizja</span><span class="sxs-lookup"><span data-stu-id="7e870-120">-Commission</span></span>
<span data-ttu-id="7e870-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7e870-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e870-122">-Decomission</span><span class="sxs-lookup"><span data-stu-id="7e870-122">-Decomission</span></span>
<span data-ttu-id="7e870-123">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7e870-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e870-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e870-124">-DefaultProfile</span></span>
<span data-ttu-id="7e870-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7e870-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e870-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7e870-126">-InputObject</span></span>
<span data-ttu-id="7e870-127">CustomIpPrefix do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="7e870-127">The CustomIpPrefix to set.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e870-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7e870-128">-Name</span></span>
<span data-ttu-id="7e870-129">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="7e870-129">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e870-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e870-130">-ResourceGroupName</span></span>
<span data-ttu-id="7e870-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7e870-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e870-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e870-132">-ResourceId</span></span>
<span data-ttu-id="7e870-133">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="7e870-133">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e870-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="7e870-134">-Tag</span></span>
<span data-ttu-id="7e870-135">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="7e870-135">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Hashtable
Parameter Sets: SetByInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e870-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7e870-136">-Confirm</span></span>
<span data-ttu-id="7e870-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e870-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e870-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e870-138">-WhatIf</span></span>
<span data-ttu-id="7e870-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e870-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e870-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7e870-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e870-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e870-141">CommonParameters</span></span>
<span data-ttu-id="7e870-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e870-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e870-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e870-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e870-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e870-144">INPUTS</span></span>

### <span data-ttu-id="7e870-145">System. String</span><span class="sxs-lookup"><span data-stu-id="7e870-145">System.String</span></span>

### <span data-ttu-id="7e870-146">Microsoft. Azure. Commands. Network. models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7e870-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

### <span data-ttu-id="7e870-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7e870-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7e870-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7e870-148">OUTPUTS</span></span>

### <span data-ttu-id="7e870-149">Microsoft. Azure. Commands. Network. models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7e870-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="7e870-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7e870-150">NOTES</span></span>

## <span data-ttu-id="7e870-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e870-151">RELATED LINKS</span></span>

[<span data-ttu-id="7e870-152">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7e870-152">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="7e870-153">Nowe — AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7e870-153">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="7e870-154">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7e870-154">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)