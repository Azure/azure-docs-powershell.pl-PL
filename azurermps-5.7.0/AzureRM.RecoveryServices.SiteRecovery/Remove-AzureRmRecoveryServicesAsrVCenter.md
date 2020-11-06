---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: eaa357e6dd216b62a2c8e8f1cd78ff15387be57a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544216"
---
# <span data-ttu-id="796de-101">Remove-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="796de-101">Remove-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="796de-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="796de-102">SYNOPSIS</span></span>
<span data-ttu-id="796de-103">Umożliwia usunięcie serwera vCenter z sieci szkieletowej ASR i zatrzymanie wykrywania maszyn wirtualnych z serwera vCenter.</span><span class="sxs-lookup"><span data-stu-id="796de-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="796de-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="796de-104">SYNTAX</span></span>

### <span data-ttu-id="796de-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="796de-105">Default (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="796de-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="796de-106">ByResourceId</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="796de-107">ByName</span><span class="sxs-lookup"><span data-stu-id="796de-107">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="796de-108">Opis</span><span class="sxs-lookup"><span data-stu-id="796de-108">DESCRIPTION</span></span>
<span data-ttu-id="796de-109">Polecenie cmdlet **Remove-AzureRmRecoveryServicesAsrvCenter** umożliwia usunięcie serwera vCenter z sieci szkieletowej ASR i zatrzymanie wykrywania maszyn wirtualnych z serwera vCenter.</span><span class="sxs-lookup"><span data-stu-id="796de-109">The **Remove-AzureRmRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="796de-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="796de-110">EXAMPLES</span></span>

### <span data-ttu-id="796de-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="796de-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="796de-112">Usuwa serwer vCenter z sieci szkieletowej ASR.</span><span class="sxs-lookup"><span data-stu-id="796de-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="796de-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="796de-113">PARAMETERS</span></span>

### <span data-ttu-id="796de-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="796de-114">-Confirm</span></span>
<span data-ttu-id="796de-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="796de-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="796de-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="796de-116">-DefaultProfile</span></span>
<span data-ttu-id="796de-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="796de-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="796de-118">-Fabric</span><span class="sxs-lookup"><span data-stu-id="796de-118">-Fabric</span></span>
<span data-ttu-id="796de-119">Obiekt sieci szkieletowej ASR reprezentujący serwer konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="796de-119">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="796de-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="796de-120">-InputObject</span></span>
<span data-ttu-id="796de-121">Obiekt vCenter programu ASR reprezentujący serwer vCenter, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="796de-121">ASR vCenter object representing the vCenter server to be removed.</span></span>

```yaml
Type: ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="796de-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="796de-122">-Name</span></span>
<span data-ttu-id="796de-123">Nazwa serwera vCenter.</span><span class="sxs-lookup"><span data-stu-id="796de-123">Name of the vCenter Server.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="796de-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="796de-124">-ResourceId</span></span>
<span data-ttu-id="796de-125">Określa identyfikator zasobu vCenter do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="796de-125">Specifies the resourceId of vCenter to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="796de-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="796de-126">-WhatIf</span></span>
<span data-ttu-id="796de-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="796de-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="796de-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="796de-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="796de-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="796de-129">CommonParameters</span></span>
<span data-ttu-id="796de-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="796de-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="796de-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="796de-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="796de-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="796de-132">INPUTS</span></span>

### <span data-ttu-id="796de-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="796de-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="796de-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="796de-134">OUTPUTS</span></span>

### <span data-ttu-id="796de-135">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="796de-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="796de-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="796de-136">NOTES</span></span>

## <span data-ttu-id="796de-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="796de-137">RELATED LINKS</span></span>
