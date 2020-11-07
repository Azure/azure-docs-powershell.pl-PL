---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 248cbd6f94a95a0024b9fb72c6a2d8dd896eb0f3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872935"
---
# <span data-ttu-id="09076-101">New-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="09076-101">New-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="09076-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="09076-102">SYNOPSIS</span></span>
<span data-ttu-id="09076-103">Tworzy kontener ochrony odzyskiwania witryny platformy Azure w określonej sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="09076-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

## <span data-ttu-id="09076-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="09076-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09076-105">Opis</span><span class="sxs-lookup"><span data-stu-id="09076-105">DESCRIPTION</span></span>
<span data-ttu-id="09076-106">Polecenie cmdlet New-AzRecoveryServicesAsrProtectionContainer tworzy kontener ochrony pod określoną siecią szkieletową odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="09076-106">The New-AzRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="09076-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="09076-107">EXAMPLES</span></span>

### <span data-ttu-id="09076-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="09076-108">Example 1</span></span>
```
PS C:\> $job = New-AzRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="09076-109">Rozpoczyna Tworzenie kontenera ochrony z określonymi parametrami i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="09076-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="09076-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="09076-110">PARAMETERS</span></span>

### <span data-ttu-id="09076-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09076-111">-DefaultProfile</span></span>
<span data-ttu-id="09076-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="09076-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09076-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="09076-113">-InputObject</span></span>
<span data-ttu-id="09076-114">Tworzy kontener ochrony replikacji w określonym obiekcie wejściowym (Azure Fabric).</span><span class="sxs-lookup"><span data-stu-id="09076-114">Creates the replication protection container in specified input Object (Azure Fabric).</span></span>

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

### <span data-ttu-id="09076-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="09076-115">-Name</span></span>
<span data-ttu-id="09076-116">Nazwa kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="09076-116">Name of the protection container.</span></span>

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

### <span data-ttu-id="09076-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="09076-117">-Confirm</span></span>
<span data-ttu-id="09076-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09076-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09076-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09076-119">-WhatIf</span></span>
<span data-ttu-id="09076-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09076-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09076-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="09076-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09076-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09076-122">CommonParameters</span></span>
<span data-ttu-id="09076-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09076-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09076-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09076-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09076-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09076-125">INPUTS</span></span>

### <span data-ttu-id="09076-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="09076-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="09076-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="09076-127">OUTPUTS</span></span>

### <span data-ttu-id="09076-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="09076-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="09076-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="09076-129">NOTES</span></span>

## <span data-ttu-id="09076-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09076-130">RELATED LINKS</span></span>
