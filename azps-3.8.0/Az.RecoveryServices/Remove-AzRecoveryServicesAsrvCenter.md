---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 775a8694df895601d953a1efd68b7a4cba57a830
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051591"
---
# <span data-ttu-id="845e0-101">Remove-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="845e0-101">Remove-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="845e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="845e0-102">SYNOPSIS</span></span>
<span data-ttu-id="845e0-103">Umożliwia usunięcie serwera vCenter z sieci szkieletowej ASR i zatrzymanie wykrywania maszyn wirtualnych z serwera vCenter.</span><span class="sxs-lookup"><span data-stu-id="845e0-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="845e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="845e0-104">SYNTAX</span></span>

### <span data-ttu-id="845e0-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="845e0-105">Default (Default)</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="845e0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="845e0-106">ByResourceId</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="845e0-107">ByName</span><span class="sxs-lookup"><span data-stu-id="845e0-107">ByName</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="845e0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="845e0-108">DESCRIPTION</span></span>
<span data-ttu-id="845e0-109">Polecenie cmdlet **Remove-AzRecoveryServicesAsrvCenter** umożliwia usunięcie serwera vCenter z sieci szkieletowej ASR i zatrzymanie wykrywania maszyn wirtualnych z serwera vCenter.</span><span class="sxs-lookup"><span data-stu-id="845e0-109">The **Remove-AzRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="845e0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="845e0-110">EXAMPLES</span></span>

### <span data-ttu-id="845e0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="845e0-111">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="845e0-112">Usuwa serwer vCenter z sieci szkieletowej ASR.</span><span class="sxs-lookup"><span data-stu-id="845e0-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="845e0-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="845e0-113">PARAMETERS</span></span>

### <span data-ttu-id="845e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="845e0-114">-DefaultProfile</span></span>
<span data-ttu-id="845e0-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="845e0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="845e0-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="845e0-116">-Fabric</span></span>
<span data-ttu-id="845e0-117">Obiekt sieci szkieletowej ASR reprezentujący serwer konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="845e0-117">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="845e0-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="845e0-118">-InputObject</span></span>
<span data-ttu-id="845e0-119">Obiekt vCenter programu ASR reprezentujący serwer vCenter, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="845e0-119">ASR vCenter object representing the vCenter server to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="845e0-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="845e0-120">-Name</span></span>
<span data-ttu-id="845e0-121">Nazwa serwera vCenter.</span><span class="sxs-lookup"><span data-stu-id="845e0-121">Name of the vCenter Server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="845e0-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="845e0-122">-ResourceId</span></span>
<span data-ttu-id="845e0-123">Określa identyfikator zasobu vCenter do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="845e0-123">Specifies the resourceId of vCenter to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="845e0-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="845e0-124">-Confirm</span></span>
<span data-ttu-id="845e0-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="845e0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="845e0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="845e0-126">-WhatIf</span></span>
<span data-ttu-id="845e0-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="845e0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="845e0-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="845e0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="845e0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="845e0-129">CommonParameters</span></span>
<span data-ttu-id="845e0-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="845e0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="845e0-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="845e0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="845e0-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="845e0-132">INPUTS</span></span>

### <span data-ttu-id="845e0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="845e0-133">System.String</span></span>

### <span data-ttu-id="845e0-134">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="845e0-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

### <span data-ttu-id="845e0-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="845e0-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="845e0-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="845e0-136">OUTPUTS</span></span>

### <span data-ttu-id="845e0-137">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="845e0-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="845e0-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="845e0-138">NOTES</span></span>

## <span data-ttu-id="845e0-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="845e0-139">RELATED LINKS</span></span>
