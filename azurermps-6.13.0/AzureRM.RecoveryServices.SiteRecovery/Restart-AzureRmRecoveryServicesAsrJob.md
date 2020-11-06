---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/restart-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 94f4f44da8da4b2ad16db6dff86ad22908847a62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552067"
---
# <span data-ttu-id="d12a5-101">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="d12a5-101">Restart-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="d12a5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d12a5-102">SYNOPSIS</span></span>
<span data-ttu-id="d12a5-103">Ponowne uruchamianie zadania odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="d12a5-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d12a5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d12a5-104">SYNTAX</span></span>

### <span data-ttu-id="d12a5-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d12a5-105">ByObject (Default)</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d12a5-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d12a5-106">ByName</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d12a5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d12a5-107">DESCRIPTION</span></span>
<span data-ttu-id="d12a5-108">Polecenie cmdlet **restart-AzureRmRecoveryServicesAsrJob** powoduje ponowne uruchomienie zadania odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="d12a5-108">The **Restart-AzureRmRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="d12a5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d12a5-109">EXAMPLES</span></span>

### <span data-ttu-id="d12a5-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d12a5-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="d12a5-111">Powoduje ponowne uruchomienie określonego zadania ASR i zwraca zaktualizowany obiekt zadania ASR zadania ASR.</span><span class="sxs-lookup"><span data-stu-id="d12a5-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="d12a5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d12a5-112">PARAMETERS</span></span>

### <span data-ttu-id="d12a5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d12a5-113">-DefaultProfile</span></span>
<span data-ttu-id="d12a5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d12a5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d12a5-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d12a5-115">-InputObject</span></span>
<span data-ttu-id="d12a5-116">Obiekt wejściowy do polecenia cmdlet: obiekt zadania ASR odpowiadający zadaniu ASR do ponownego uruchomienia</span><span class="sxs-lookup"><span data-stu-id="d12a5-116">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>


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

### <span data-ttu-id="d12a5-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d12a5-117">-Name</span></span>
<span data-ttu-id="d12a5-118">Określ zadanie według nazwy.</span><span class="sxs-lookup"><span data-stu-id="d12a5-118">Specify the job by name.</span></span>

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

### <span data-ttu-id="d12a5-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d12a5-119">-Confirm</span></span>
<span data-ttu-id="d12a5-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d12a5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d12a5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d12a5-121">-WhatIf</span></span>
<span data-ttu-id="d12a5-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d12a5-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d12a5-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d12a5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d12a5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d12a5-124">CommonParameters</span></span>
<span data-ttu-id="d12a5-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d12a5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d12a5-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d12a5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d12a5-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d12a5-127">INPUTS</span></span>

### <span data-ttu-id="d12a5-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d12a5-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d12a5-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d12a5-129">OUTPUTS</span></span>

### <span data-ttu-id="d12a5-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d12a5-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d12a5-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d12a5-131">NOTES</span></span>

## <span data-ttu-id="d12a5-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d12a5-132">RELATED LINKS</span></span>

[<span data-ttu-id="d12a5-133">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="d12a5-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="d12a5-134">Życiorys — AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="d12a5-134">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="d12a5-135">Zatrzymaj — AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="d12a5-135">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
