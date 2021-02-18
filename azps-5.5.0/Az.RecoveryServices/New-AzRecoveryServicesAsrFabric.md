---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: e1966e7172bcce724702b8652b5e85fcce79260e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192890"
---
# <span data-ttu-id="6b1e0-101">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="6b1e0-101">New-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="6b1e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b1e0-102">SYNOPSIS</span></span>
<span data-ttu-id="6b1e0-103">Tworzy szkielet odzyskiwania witryn platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6b1e0-103">Creates an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="6b1e0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6b1e0-104">SYNTAX</span></span>

### <span data-ttu-id="6b1e0-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="6b1e0-105">Default (Default)</span></span>
```
New-AzRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b1e0-106">Azure</span><span class="sxs-lookup"><span data-stu-id="6b1e0-106">Azure</span></span>
```
New-AzRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b1e0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="6b1e0-107">DESCRIPTION</span></span>
<span data-ttu-id="6b1e0-108">Polecenie **cmdlet New-AzRecoveryServicesAsrFabric** tworzy element Azure Site Recovery Fabric określonego typu.</span><span class="sxs-lookup"><span data-stu-id="6b1e0-108">The **New-AzRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="6b1e0-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6b1e0-109">EXAMPLES</span></span>

### <span data-ttu-id="6b1e0-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6b1e0-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="6b1e0-111">Rozpoczyna tworzenie szkieletów z minąłem i zwraca zadanie asr służące do śledzenia operacji tworzenia materiału.</span><span class="sxs-lookup"><span data-stu-id="6b1e0-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="6b1e0-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6b1e0-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="6b1e0-113">Rozpoczyna tworzenie szkieletów azure z minąłem i zwraca zadanie asr służące do śledzenia operacji tworzenia materiału.</span><span class="sxs-lookup"><span data-stu-id="6b1e0-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="6b1e0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b1e0-114">PARAMETERS</span></span>

### <span data-ttu-id="6b1e0-115">— Azure</span><span class="sxs-lookup"><span data-stu-id="6b1e0-115">-Azure</span></span>
<span data-ttu-id="6b1e0-116">Parametr przełącznika służy do tworzenia azure fabric.</span><span class="sxs-lookup"><span data-stu-id="6b1e0-116">Switch parameter specifies to create azure fabric.</span></span>

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

### <span data-ttu-id="6b1e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b1e0-117">-DefaultProfile</span></span>
<span data-ttu-id="6b1e0-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6b1e0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6b1e0-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6b1e0-119">-Location</span></span>
<span data-ttu-id="6b1e0-120">Określa region platformy Azure odpowiadający tworzonego obiektu Fabric.</span><span class="sxs-lookup"><span data-stu-id="6b1e0-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="6b1e0-121">Obiekt szkieletowy usługi Azure Site Recovery reprezentuje region.</span><span class="sxs-lookup"><span data-stu-id="6b1e0-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="6b1e0-122">W przypadku maszyn wirtualnych replikowanych między dwoma regionami platformy Azure podstawowa sieć szkieletowa reprezentuje podstawowy region platformy Azure i sieć szkieletową odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6b1e0-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

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

### <span data-ttu-id="6b1e0-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6b1e0-123">-Name</span></span>
<span data-ttu-id="6b1e0-124">Określa nazwę sieci Azure Site Recovery Fabric.</span><span class="sxs-lookup"><span data-stu-id="6b1e0-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="6b1e0-125">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="6b1e0-125">-Type</span></span>
<span data-ttu-id="6b1e0-126">Określa typ szkieletu odzyskiwania witryn platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6b1e0-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

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

### <span data-ttu-id="6b1e0-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6b1e0-127">-Confirm</span></span>
<span data-ttu-id="6b1e0-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6b1e0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b1e0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b1e0-129">-WhatIf</span></span>
<span data-ttu-id="6b1e0-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b1e0-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6b1e0-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6b1e0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b1e0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b1e0-132">CommonParameters</span></span>
<span data-ttu-id="6b1e0-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b1e0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b1e0-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b1e0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b1e0-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b1e0-135">INPUTS</span></span>

### <span data-ttu-id="6b1e0-136">Brak</span><span class="sxs-lookup"><span data-stu-id="6b1e0-136">None</span></span>

## <span data-ttu-id="6b1e0-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b1e0-137">OUTPUTS</span></span>

### <span data-ttu-id="6b1e0-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="6b1e0-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6b1e0-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6b1e0-139">NOTES</span></span>

## <span data-ttu-id="6b1e0-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b1e0-140">RELATED LINKS</span></span>

[<span data-ttu-id="6b1e0-141">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="6b1e0-141">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="6b1e0-142">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="6b1e0-142">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
