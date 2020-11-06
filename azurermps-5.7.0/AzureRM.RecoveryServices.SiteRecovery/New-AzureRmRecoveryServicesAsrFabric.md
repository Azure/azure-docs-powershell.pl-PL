---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 53398a882ff513443f8eae336539858f7fe34ce4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548048"
---
# <span data-ttu-id="21e86-101">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="21e86-101">New-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="21e86-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21e86-102">SYNOPSIS</span></span>
<span data-ttu-id="21e86-103">Tworzy sieć szkieletową odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="21e86-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21e86-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21e86-104">SYNTAX</span></span>

### <span data-ttu-id="21e86-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="21e86-105">Default (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21e86-106">Azure</span><span class="sxs-lookup"><span data-stu-id="21e86-106">Azure</span></span>
```
New-AzureRmRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21e86-107">Opis</span><span class="sxs-lookup"><span data-stu-id="21e86-107">DESCRIPTION</span></span>
<span data-ttu-id="21e86-108">Polecenie cmdlet **New-AzureRmRecoveryServicesAsrFabric** umożliwia utworzenie sieci szkieletowej odzyskiwania witryny platformy Azure określonego typu.</span><span class="sxs-lookup"><span data-stu-id="21e86-108">The **New-AzureRmRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="21e86-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21e86-109">EXAMPLES</span></span>

### <span data-ttu-id="21e86-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="21e86-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="21e86-111">Rozpoczyna tworzenie sieci szkieletowej z przekazaną nazwą i zwraca zadanie ASR używane do śledzenia operacji tworzenia sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="21e86-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="21e86-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="21e86-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="21e86-113">Rozpoczyna Tworzenie usługi Azure Fabric z przekazaną nazwą i zwraca zadanie ASR używane do śledzenia operacji tworzenia sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="21e86-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="21e86-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21e86-114">PARAMETERS</span></span>

### <span data-ttu-id="21e86-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="21e86-115">-Azure</span></span>
<span data-ttu-id="21e86-116">Parametr Switch wskazuje możliwość utworzenia sieci Azure Fabric.</span><span class="sxs-lookup"><span data-stu-id="21e86-116">Switch parameter indicates creation of azure fabric.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e86-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="21e86-117">-Confirm</span></span>
<span data-ttu-id="21e86-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21e86-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21e86-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21e86-119">-DefaultProfile</span></span>
<span data-ttu-id="21e86-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="21e86-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="21e86-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="21e86-121">-Location</span></span>
<span data-ttu-id="21e86-122">Określa obszar Azure odpowiadający tworzonemu obiektowi sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="21e86-122">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="21e86-123">Obiekt szkieletu usługi Azure Site Recovery reprezentuje region.</span><span class="sxs-lookup"><span data-stu-id="21e86-123">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="21e86-124">W przypadku replikowanych maszyn wirtualnych między dwoma regionami platformy Azure podstawowa Sieć szkieletowa reprezentuje podstawowy region platformy Azure i szkielet odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="21e86-124">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

```yaml
Type: String
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e86-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="21e86-125">-Name</span></span>
<span data-ttu-id="21e86-126">Określa nazwę sieci szkieletowej odzyskiwania witryny usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="21e86-126">Specifies the name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e86-127">-Type</span><span class="sxs-lookup"><span data-stu-id="21e86-127">-Type</span></span>
<span data-ttu-id="21e86-128">Określa typ sieci szkieletowej usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="21e86-128">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e86-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21e86-129">-WhatIf</span></span>
<span data-ttu-id="21e86-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21e86-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21e86-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="21e86-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21e86-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21e86-132">CommonParameters</span></span>
<span data-ttu-id="21e86-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21e86-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21e86-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21e86-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21e86-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21e86-135">INPUTS</span></span>

### <span data-ttu-id="21e86-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="21e86-136">None</span></span>

## <span data-ttu-id="21e86-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21e86-137">OUTPUTS</span></span>

### <span data-ttu-id="21e86-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="21e86-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="21e86-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21e86-139">NOTES</span></span>

## <span data-ttu-id="21e86-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21e86-140">RELATED LINKS</span></span>

[<span data-ttu-id="21e86-141">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="21e86-141">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="21e86-142">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="21e86-142">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
