---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
ms.openlocfilehash: 3a83b7200f7634574fd457d2fa08f926a62b9a82
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370951"
---
# <span data-ttu-id="6dc7d-101">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6dc7d-101">Remove-AzNetworkProfile</span></span>

## <span data-ttu-id="6dc7d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6dc7d-102">SYNOPSIS</span></span>
<span data-ttu-id="6dc7d-103">Usuwa profil sieciowy.</span><span class="sxs-lookup"><span data-stu-id="6dc7d-103">Removes a network profile.</span></span>

## <span data-ttu-id="6dc7d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6dc7d-104">SYNTAX</span></span>

### <span data-ttu-id="6dc7d-105">RemoveByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6dc7d-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dc7d-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6dc7d-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dc7d-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6dc7d-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dc7d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6dc7d-108">DESCRIPTION</span></span>
<span data-ttu-id="6dc7d-109">Polecenie cmdlet **Remove-AzNetworkProfile** usuwa profil sieciowy, jeśli nie utworzono interfejsów sieciowych kontenera (w przeciwieństwie do **konfiguracji** interfejsu sieciowego kontenera).</span><span class="sxs-lookup"><span data-stu-id="6dc7d-109">The **Remove-AzNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration**) have been created.</span></span>

## <span data-ttu-id="6dc7d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6dc7d-110">EXAMPLES</span></span>

### <span data-ttu-id="6dc7d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6dc7d-111">Example 1</span></span>
```powershell
Remove-AzNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="6dc7d-112">Spowoduje to usunięcie profilu sieciowego z nazwą NP1 z RG1 grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6dc7d-112">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="6dc7d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6dc7d-113">PARAMETERS</span></span>

### <span data-ttu-id="6dc7d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6dc7d-114">-AsJob</span></span>
<span data-ttu-id="6dc7d-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6dc7d-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dc7d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dc7d-116">-DefaultProfile</span></span>
<span data-ttu-id="6dc7d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6dc7d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dc7d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6dc7d-118">-Force</span></span>
<span data-ttu-id="6dc7d-119">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób</span><span class="sxs-lookup"><span data-stu-id="6dc7d-119">Do not ask for confirmation if you want to delete resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dc7d-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6dc7d-120">-InputObject</span></span>
<span data-ttu-id="6dc7d-121">Obiekt profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="6dc7d-121">Network profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6dc7d-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6dc7d-122">-Name</span></span>
<span data-ttu-id="6dc7d-123">Nazwa profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="6dc7d-123">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dc7d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6dc7d-124">-PassThru</span></span>
<span data-ttu-id="6dc7d-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="6dc7d-125">Returns an object representing the item with which you are working.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dc7d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dc7d-126">-ResourceGroupName</span></span>
<span data-ttu-id="6dc7d-127">Nazwa grupy zasobów profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="6dc7d-127">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dc7d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6dc7d-128">-ResourceId</span></span>
<span data-ttu-id="6dc7d-129">Identyfikator zasobu Menedżera zasobów platformy Azure profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="6dc7d-129">The Azure resource manager resource ID of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dc7d-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6dc7d-130">-Confirm</span></span>
<span data-ttu-id="6dc7d-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dc7d-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dc7d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dc7d-132">-WhatIf</span></span>
<span data-ttu-id="6dc7d-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dc7d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dc7d-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6dc7d-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dc7d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dc7d-135">CommonParameters</span></span>
<span data-ttu-id="6dc7d-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dc7d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dc7d-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dc7d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dc7d-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6dc7d-138">INPUTS</span></span>

### <span data-ttu-id="6dc7d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6dc7d-139">System.String</span></span>

### <span data-ttu-id="6dc7d-140">Microsoft. Azure. Commands. Network. models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6dc7d-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="6dc7d-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6dc7d-141">OUTPUTS</span></span>

### <span data-ttu-id="6dc7d-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6dc7d-142">System.Boolean</span></span>

## <span data-ttu-id="6dc7d-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6dc7d-143">NOTES</span></span>

## <span data-ttu-id="6dc7d-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6dc7d-144">RELATED LINKS</span></span>

[<span data-ttu-id="6dc7d-145">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6dc7d-145">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="6dc7d-146">Nowe — AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6dc7d-146">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="6dc7d-147">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6dc7d-147">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
