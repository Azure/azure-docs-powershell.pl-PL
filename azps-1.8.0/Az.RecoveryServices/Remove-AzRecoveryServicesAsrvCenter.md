---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: c1ac3ae34e92feb2b356d5946a7b9f0a30a0a2aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708590"
---
# <span data-ttu-id="fec73-101">Remove-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="fec73-101">Remove-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="fec73-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fec73-102">SYNOPSIS</span></span>
<span data-ttu-id="fec73-103">Umożliwia usunięcie serwera vCenter z sieci szkieletowej ASR i zatrzymanie wykrywania maszyn wirtualnych z serwera vCenter.</span><span class="sxs-lookup"><span data-stu-id="fec73-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="fec73-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fec73-104">SYNTAX</span></span>

### <span data-ttu-id="fec73-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="fec73-105">Default (Default)</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fec73-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fec73-106">ByResourceId</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fec73-107">ByName</span><span class="sxs-lookup"><span data-stu-id="fec73-107">ByName</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fec73-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fec73-108">DESCRIPTION</span></span>
<span data-ttu-id="fec73-109">Polecenie cmdlet **Remove-AzRecoveryServicesAsrvCenter** umożliwia usunięcie serwera vCenter z sieci szkieletowej ASR i zatrzymanie wykrywania maszyn wirtualnych z serwera vCenter.</span><span class="sxs-lookup"><span data-stu-id="fec73-109">The **Remove-AzRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="fec73-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fec73-110">EXAMPLES</span></span>

### <span data-ttu-id="fec73-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fec73-111">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="fec73-112">Usuwa serwer vCenter z sieci szkieletowej ASR.</span><span class="sxs-lookup"><span data-stu-id="fec73-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="fec73-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fec73-113">PARAMETERS</span></span>

### <span data-ttu-id="fec73-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fec73-114">-DefaultProfile</span></span>
<span data-ttu-id="fec73-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fec73-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fec73-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="fec73-116">-Fabric</span></span>
<span data-ttu-id="fec73-117">Obiekt sieci szkieletowej ASR reprezentujący serwer konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="fec73-117">ASR fabric object representing the Configuration Server.</span></span>

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

### <span data-ttu-id="fec73-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fec73-118">-InputObject</span></span>
<span data-ttu-id="fec73-119">Obiekt vCenter programu ASR reprezentujący serwer vCenter, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="fec73-119">ASR vCenter object representing the vCenter server to be removed.</span></span>

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

### <span data-ttu-id="fec73-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fec73-120">-Name</span></span>
<span data-ttu-id="fec73-121">Nazwa serwera vCenter.</span><span class="sxs-lookup"><span data-stu-id="fec73-121">Name of the vCenter Server.</span></span>

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

### <span data-ttu-id="fec73-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fec73-122">-ResourceId</span></span>
<span data-ttu-id="fec73-123">Określa identyfikator zasobu vCenter do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="fec73-123">Specifies the resourceId of vCenter to remove.</span></span>

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

### <span data-ttu-id="fec73-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fec73-124">-Confirm</span></span>
<span data-ttu-id="fec73-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fec73-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fec73-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fec73-126">-WhatIf</span></span>
<span data-ttu-id="fec73-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fec73-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fec73-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fec73-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fec73-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fec73-129">CommonParameters</span></span>
<span data-ttu-id="fec73-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fec73-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fec73-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fec73-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fec73-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fec73-132">INPUTS</span></span>

### <span data-ttu-id="fec73-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fec73-133">System.String</span></span>

### <span data-ttu-id="fec73-134">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="fec73-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

### <span data-ttu-id="fec73-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="fec73-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="fec73-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fec73-136">OUTPUTS</span></span>

### <span data-ttu-id="fec73-137">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="fec73-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fec73-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fec73-138">NOTES</span></span>

## <span data-ttu-id="fec73-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fec73-139">RELATED LINKS</span></span>
