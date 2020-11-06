---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 505d2d81eefed3132cd693ea6cd989fde173b8b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552071"
---
# <span data-ttu-id="e3eac-101">Remove-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="e3eac-101">Remove-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="e3eac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e3eac-102">SYNOPSIS</span></span>
<span data-ttu-id="e3eac-103">Umożliwia usunięcie serwera vCenter z sieci szkieletowej ASR i zatrzymanie wykrywania maszyn wirtualnych z serwera vCenter.</span><span class="sxs-lookup"><span data-stu-id="e3eac-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3eac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e3eac-104">SYNTAX</span></span>

### <span data-ttu-id="e3eac-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="e3eac-105">Default (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3eac-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e3eac-106">ByResourceId</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3eac-107">ByName</span><span class="sxs-lookup"><span data-stu-id="e3eac-107">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3eac-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e3eac-108">DESCRIPTION</span></span>
<span data-ttu-id="e3eac-109">Polecenie cmdlet **Remove-AzureRmRecoveryServicesAsrvCenter** umożliwia usunięcie serwera vCenter z sieci szkieletowej ASR i zatrzymanie wykrywania maszyn wirtualnych z serwera vCenter.</span><span class="sxs-lookup"><span data-stu-id="e3eac-109">The **Remove-AzureRmRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="e3eac-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e3eac-110">EXAMPLES</span></span>

### <span data-ttu-id="e3eac-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e3eac-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="e3eac-112">Usuwa serwer vCenter z sieci szkieletowej ASR.</span><span class="sxs-lookup"><span data-stu-id="e3eac-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="e3eac-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3eac-113">PARAMETERS</span></span>

### <span data-ttu-id="e3eac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3eac-114">-DefaultProfile</span></span>
<span data-ttu-id="e3eac-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e3eac-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3eac-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="e3eac-116">-Fabric</span></span>
<span data-ttu-id="e3eac-117">Obiekt sieci szkieletowej ASR reprezentujący serwer konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="e3eac-117">ASR fabric object representing the Configuration Server.</span></span>

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

### <span data-ttu-id="e3eac-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e3eac-118">-InputObject</span></span>
<span data-ttu-id="e3eac-119">Obiekt vCenter programu ASR reprezentujący serwer vCenter, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="e3eac-119">ASR vCenter object representing the vCenter server to be removed.</span></span>

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

### <span data-ttu-id="e3eac-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e3eac-120">-Name</span></span>
<span data-ttu-id="e3eac-121">Nazwa serwera vCenter.</span><span class="sxs-lookup"><span data-stu-id="e3eac-121">Name of the vCenter Server.</span></span>

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

### <span data-ttu-id="e3eac-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3eac-122">-ResourceId</span></span>
<span data-ttu-id="e3eac-123">Określa identyfikator zasobu vCenter do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e3eac-123">Specifies the resourceId of vCenter to remove.</span></span>

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

### <span data-ttu-id="e3eac-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e3eac-124">-Confirm</span></span>
<span data-ttu-id="e3eac-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3eac-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3eac-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3eac-126">-WhatIf</span></span>
<span data-ttu-id="e3eac-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3eac-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3eac-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e3eac-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3eac-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3eac-129">CommonParameters</span></span>
<span data-ttu-id="e3eac-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3eac-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3eac-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3eac-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3eac-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3eac-132">INPUTS</span></span>

### <span data-ttu-id="e3eac-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="e3eac-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="e3eac-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e3eac-134">OUTPUTS</span></span>

### <span data-ttu-id="e3eac-135">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e3eac-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e3eac-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e3eac-136">NOTES</span></span>

## <span data-ttu-id="e3eac-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3eac-137">RELATED LINKS</span></span>
