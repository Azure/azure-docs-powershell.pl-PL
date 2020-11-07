---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/stop-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 14f24f9b9659b6668041b800462eca422fb67c97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716568"
---
# <span data-ttu-id="e741b-101">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="e741b-101">Stop-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="e741b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e741b-102">SYNOPSIS</span></span>
<span data-ttu-id="e741b-103">Zatrzymuje zadanie odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="e741b-103">Stops an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e741b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e741b-104">SYNTAX</span></span>

### <span data-ttu-id="e741b-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e741b-105">ByObject (Default)</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e741b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e741b-106">ByName</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e741b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e741b-107">DESCRIPTION</span></span>
<span data-ttu-id="e741b-108">Polecenie cmdlet **stop-AzureRmRecoveryServicesAsrJob** zatrzymuje określone zadanie odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e741b-108">The **Stop-AzureRmRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="e741b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e741b-109">EXAMPLES</span></span>

### <span data-ttu-id="e741b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e741b-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="e741b-111">Próbuje zatrzymać określone zadanie i zwraca zaktualizowany obiekt zadania ASR.</span><span class="sxs-lookup"><span data-stu-id="e741b-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="e741b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e741b-112">PARAMETERS</span></span>

### <span data-ttu-id="e741b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e741b-113">-DefaultProfile</span></span>
<span data-ttu-id="e741b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e741b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e741b-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e741b-115">-InputObject</span></span>
<span data-ttu-id="e741b-116">Obiekt wejściowy: Określ obiekt zadania ASR odpowiadający zadaniu funkcji ASR, który ma zostać zatrzymany</span><span class="sxs-lookup"><span data-stu-id="e741b-116">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

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

### <span data-ttu-id="e741b-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e741b-117">-Name</span></span>
<span data-ttu-id="e741b-118">Określ zadanie ASR, które ma zostać zatrzymane przez nazwę zadania ASR.</span><span class="sxs-lookup"><span data-stu-id="e741b-118">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="e741b-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e741b-119">-Confirm</span></span>
<span data-ttu-id="e741b-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e741b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e741b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e741b-121">-WhatIf</span></span>
<span data-ttu-id="e741b-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e741b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e741b-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e741b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e741b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e741b-124">CommonParameters</span></span>
<span data-ttu-id="e741b-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e741b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e741b-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e741b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e741b-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e741b-127">INPUTS</span></span>

### <span data-ttu-id="e741b-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e741b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e741b-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e741b-129">OUTPUTS</span></span>

### <span data-ttu-id="e741b-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e741b-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e741b-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e741b-131">NOTES</span></span>

## <span data-ttu-id="e741b-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e741b-132">RELATED LINKS</span></span>

[<span data-ttu-id="e741b-133">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="e741b-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="e741b-134">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="e741b-134">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="e741b-135">Życiorys — AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="e741b-135">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)
