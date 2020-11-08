---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: a86e58fe3c933ffaa9a382dc1e5140d3b42a34cb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225815"
---
# <span data-ttu-id="05cdb-101">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="05cdb-101">Stop-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="05cdb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="05cdb-102">SYNOPSIS</span></span>
<span data-ttu-id="05cdb-103">Zatrzymuje zadanie odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="05cdb-103">Stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="05cdb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="05cdb-104">SYNTAX</span></span>

### <span data-ttu-id="05cdb-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="05cdb-105">ByObject (Default)</span></span>
```
Stop-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05cdb-106">ByName</span><span class="sxs-lookup"><span data-stu-id="05cdb-106">ByName</span></span>
```
Stop-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05cdb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="05cdb-107">DESCRIPTION</span></span>
<span data-ttu-id="05cdb-108">Polecenie cmdlet **stop-AzRecoveryServicesAsrJob** zatrzymuje określone zadanie odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="05cdb-108">The **Stop-AzRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="05cdb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="05cdb-109">EXAMPLES</span></span>

### <span data-ttu-id="05cdb-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="05cdb-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="05cdb-111">Próbuje zatrzymać określone zadanie i zwraca zaktualizowany obiekt zadania ASR.</span><span class="sxs-lookup"><span data-stu-id="05cdb-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="05cdb-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="05cdb-112">PARAMETERS</span></span>

### <span data-ttu-id="05cdb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05cdb-113">-DefaultProfile</span></span>
<span data-ttu-id="05cdb-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="05cdb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="05cdb-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="05cdb-115">-InputObject</span></span>
<span data-ttu-id="05cdb-116">Obiekt wejściowy: Określ obiekt zadania ASR odpowiadający zadaniu funkcji ASR, który ma zostać zatrzymany</span><span class="sxs-lookup"><span data-stu-id="05cdb-116">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05cdb-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="05cdb-117">-Name</span></span>
<span data-ttu-id="05cdb-118">Określ zadanie ASR, które ma zostać zatrzymane przez nazwę zadania ASR.</span><span class="sxs-lookup"><span data-stu-id="05cdb-118">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="05cdb-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="05cdb-119">-Confirm</span></span>
<span data-ttu-id="05cdb-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05cdb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05cdb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05cdb-121">-WhatIf</span></span>
<span data-ttu-id="05cdb-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05cdb-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="05cdb-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="05cdb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05cdb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05cdb-124">CommonParameters</span></span>
<span data-ttu-id="05cdb-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05cdb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05cdb-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05cdb-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05cdb-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05cdb-127">INPUTS</span></span>

### <span data-ttu-id="05cdb-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="05cdb-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="05cdb-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="05cdb-129">OUTPUTS</span></span>

### <span data-ttu-id="05cdb-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="05cdb-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="05cdb-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="05cdb-131">NOTES</span></span>

## <span data-ttu-id="05cdb-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05cdb-132">RELATED LINKS</span></span>

[<span data-ttu-id="05cdb-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="05cdb-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="05cdb-134">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="05cdb-134">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="05cdb-135">Życiorys — AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="05cdb-135">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)
