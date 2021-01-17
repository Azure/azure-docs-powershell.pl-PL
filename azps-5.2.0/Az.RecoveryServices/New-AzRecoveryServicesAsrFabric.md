---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: e1966e7172bcce724702b8652b5e85fcce79260e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340693"
---
# <span data-ttu-id="13eda-101">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="13eda-101">New-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="13eda-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13eda-102">SYNOPSIS</span></span>
<span data-ttu-id="13eda-103">Tworzy sieć szkieletową odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="13eda-103">Creates an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="13eda-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13eda-104">SYNTAX</span></span>

### <span data-ttu-id="13eda-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="13eda-105">Default (Default)</span></span>
```
New-AzRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13eda-106">Azure</span><span class="sxs-lookup"><span data-stu-id="13eda-106">Azure</span></span>
```
New-AzRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13eda-107">Opis</span><span class="sxs-lookup"><span data-stu-id="13eda-107">DESCRIPTION</span></span>
<span data-ttu-id="13eda-108">Polecenie cmdlet **New-AzRecoveryServicesAsrFabric** umożliwia utworzenie sieci szkieletowej odzyskiwania witryny platformy Azure określonego typu.</span><span class="sxs-lookup"><span data-stu-id="13eda-108">The **New-AzRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="13eda-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13eda-109">EXAMPLES</span></span>

### <span data-ttu-id="13eda-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="13eda-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="13eda-111">Rozpoczyna tworzenie sieci szkieletowej z przekazaną nazwą i zwraca zadanie ASR używane do śledzenia operacji tworzenia sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="13eda-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="13eda-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="13eda-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="13eda-113">Rozpoczyna Tworzenie usługi Azure Fabric z przekazaną nazwą i zwraca zadanie ASR używane do śledzenia operacji tworzenia sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="13eda-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="13eda-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13eda-114">PARAMETERS</span></span>

### <span data-ttu-id="13eda-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="13eda-115">-Azure</span></span>
<span data-ttu-id="13eda-116">Parametr Switch określa, aby utworzyć usługę Azure Fabric.</span><span class="sxs-lookup"><span data-stu-id="13eda-116">Switch parameter specifies to create azure fabric.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13eda-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13eda-117">-DefaultProfile</span></span>
<span data-ttu-id="13eda-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="13eda-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="13eda-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="13eda-119">-Location</span></span>
<span data-ttu-id="13eda-120">Określa obszar Azure odpowiadający tworzonemu obiektowi sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="13eda-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="13eda-121">Obiekt szkieletu usługi Azure Site Recovery reprezentuje region.</span><span class="sxs-lookup"><span data-stu-id="13eda-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="13eda-122">W przypadku replikowanych maszyn wirtualnych między dwoma regionami platformy Azure podstawowa Sieć szkieletowa reprezentuje podstawowy region platformy Azure i szkielet odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="13eda-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

```yaml
Type: System.String
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13eda-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="13eda-123">-Name</span></span>
<span data-ttu-id="13eda-124">Określa nazwę sieci szkieletowej odzyskiwania witryny usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="13eda-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13eda-125">-Type</span><span class="sxs-lookup"><span data-stu-id="13eda-125">-Type</span></span>
<span data-ttu-id="13eda-126">Określa typ sieci szkieletowej usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="13eda-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13eda-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13eda-127">-Confirm</span></span>
<span data-ttu-id="13eda-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13eda-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13eda-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13eda-129">-WhatIf</span></span>
<span data-ttu-id="13eda-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13eda-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13eda-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="13eda-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13eda-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13eda-132">CommonParameters</span></span>
<span data-ttu-id="13eda-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13eda-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13eda-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13eda-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13eda-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13eda-135">INPUTS</span></span>

### <span data-ttu-id="13eda-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="13eda-136">None</span></span>

## <span data-ttu-id="13eda-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13eda-137">OUTPUTS</span></span>

### <span data-ttu-id="13eda-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="13eda-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="13eda-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13eda-139">NOTES</span></span>

## <span data-ttu-id="13eda-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13eda-140">RELATED LINKS</span></span>

[<span data-ttu-id="13eda-141">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="13eda-141">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="13eda-142">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="13eda-142">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
