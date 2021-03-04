---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 22ade5e749909683ff2de93065ccf458ab2ec73f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956714"
---
# <span data-ttu-id="cafde-101">New-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="cafde-101">New-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="cafde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cafde-102">SYNOPSIS</span></span>
<span data-ttu-id="cafde-103">Tworzy kontener Azure Site Recovery Protection Container w określonym szkieletie.</span><span class="sxs-lookup"><span data-stu-id="cafde-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

## <span data-ttu-id="cafde-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cafde-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cafde-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="cafde-105">DESCRIPTION</span></span>
<span data-ttu-id="cafde-106">Polecenie New-AzRecoveryServicesAsrProtectionContainer cmdlet tworzy kontener ochrony w określonym systemie Azure Site Recovery Fabric.</span><span class="sxs-lookup"><span data-stu-id="cafde-106">The New-AzRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="cafde-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cafde-107">EXAMPLES</span></span>

### <span data-ttu-id="cafde-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cafde-108">Example 1</span></span>
```
PS C:\> $job = New-AzRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="cafde-109">Rozpoczyna tworzenie kontenera ochrony z określonymi parametrami i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="cafde-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="cafde-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cafde-110">PARAMETERS</span></span>

### <span data-ttu-id="cafde-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cafde-111">-DefaultProfile</span></span>
<span data-ttu-id="cafde-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cafde-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cafde-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cafde-113">-InputObject</span></span>
<span data-ttu-id="cafde-114">Tworzy kontener ochrony replikacji w określonym obiekcie wejściowym (Azure Fabric).</span><span class="sxs-lookup"><span data-stu-id="cafde-114">Creates the replication protection container in specified input Object (Azure Fabric).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cafde-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cafde-115">-Name</span></span>
<span data-ttu-id="cafde-116">Nazwa kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="cafde-116">Name of the protection container.</span></span>

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

### <span data-ttu-id="cafde-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cafde-117">-Confirm</span></span>
<span data-ttu-id="cafde-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cafde-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cafde-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cafde-119">-WhatIf</span></span>
<span data-ttu-id="cafde-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cafde-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cafde-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cafde-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cafde-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cafde-122">CommonParameters</span></span>
<span data-ttu-id="cafde-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cafde-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cafde-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cafde-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cafde-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cafde-125">INPUTS</span></span>

### <span data-ttu-id="cafde-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="cafde-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="cafde-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cafde-127">OUTPUTS</span></span>

### <span data-ttu-id="cafde-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="cafde-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="cafde-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cafde-129">NOTES</span></span>

## <span data-ttu-id="cafde-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cafde-130">RELATED LINKS</span></span>
