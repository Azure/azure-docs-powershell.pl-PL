---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkProfile.md
ms.openlocfilehash: ebf2a58530f1dabe0e320dd78a38c63c86565c73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718806"
---
# <span data-ttu-id="356e2-101">Remove-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="356e2-101">Remove-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="356e2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="356e2-102">SYNOPSIS</span></span>
<span data-ttu-id="356e2-103">Usuwa profil sieciowy.</span><span class="sxs-lookup"><span data-stu-id="356e2-103">Removes a network profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="356e2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="356e2-104">SYNTAX</span></span>

### <span data-ttu-id="356e2-105">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="356e2-105">RemoveByName</span></span>
```
Remove-AzureRmNetworkProfile -ResourceGroupName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="356e2-106">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="356e2-106">RemoveByNameParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="356e2-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="356e2-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="356e2-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="356e2-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="356e2-109">Opis</span><span class="sxs-lookup"><span data-stu-id="356e2-109">DESCRIPTION</span></span>
<span data-ttu-id="356e2-110">Polecenie cmdlet **Remove-AzureRmNetworkProfile** usuwa profil sieciowy, jeśli nie utworzono interfejsów sieciowych kontenera (w przeciwieństwie do **konfiguracji** interfejsu sieciowego kontenera).</span><span class="sxs-lookup"><span data-stu-id="356e2-110">The **Remove-AzureRmNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration** ) have been created.</span></span>

## <span data-ttu-id="356e2-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="356e2-111">EXAMPLES</span></span>

### <span data-ttu-id="356e2-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="356e2-112">Example 1</span></span>
```powershell
Remove-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="356e2-113">Spowoduje to usunięcie profilu sieciowego z nazwą NP1 z RG1 grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="356e2-113">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="356e2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="356e2-114">PARAMETERS</span></span>

### <span data-ttu-id="356e2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="356e2-115">-AsJob</span></span>
<span data-ttu-id="356e2-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="356e2-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="356e2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="356e2-117">-DefaultProfile</span></span>
<span data-ttu-id="356e2-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="356e2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="356e2-119">-Force</span><span class="sxs-lookup"><span data-stu-id="356e2-119">-Force</span></span>
<span data-ttu-id="356e2-120">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób</span><span class="sxs-lookup"><span data-stu-id="356e2-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="356e2-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="356e2-121">-InputObject</span></span>
<span data-ttu-id="356e2-122">Obiekt profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="356e2-122">Network profile object.</span></span>

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

### <span data-ttu-id="356e2-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="356e2-123">-Name</span></span>
<span data-ttu-id="356e2-124">Nazwa profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="356e2-124">The name of the network profile.</span></span>

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

### <span data-ttu-id="356e2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="356e2-125">-PassThru</span></span>
<span data-ttu-id="356e2-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="356e2-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="356e2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="356e2-127">-ResourceGroupName</span></span>
<span data-ttu-id="356e2-128">Nazwa grupy zasobów profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="356e2-128">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="356e2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="356e2-129">-ResourceId</span></span>
<span data-ttu-id="356e2-130">Identyfikator zasobu Menedżera zasobów platformy Azure profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="356e2-130">The Azure resource manager resource ID of the network profile.</span></span>

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

### <span data-ttu-id="356e2-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="356e2-131">-Confirm</span></span>
<span data-ttu-id="356e2-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="356e2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="356e2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="356e2-133">-WhatIf</span></span>
<span data-ttu-id="356e2-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="356e2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="356e2-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="356e2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="356e2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="356e2-136">CommonParameters</span></span>
<span data-ttu-id="356e2-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="356e2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="356e2-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="356e2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="356e2-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="356e2-139">INPUTS</span></span>

### <span data-ttu-id="356e2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="356e2-140">System.String</span></span>

## <span data-ttu-id="356e2-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="356e2-141">OUTPUTS</span></span>

### <span data-ttu-id="356e2-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="356e2-142">System.Boolean</span></span>

## <span data-ttu-id="356e2-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="356e2-143">NOTES</span></span>

## <span data-ttu-id="356e2-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="356e2-144">RELATED LINKS</span></span>
