---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/stop-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: c573cd8162961660dac57be3d3f5fe18cd055a89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524998"
---
# <span data-ttu-id="53a9c-101">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="53a9c-101">Stop-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="53a9c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="53a9c-102">SYNOPSIS</span></span>
<span data-ttu-id="53a9c-103">Zatrzymuje zadanie odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="53a9c-103">Stops an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53a9c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="53a9c-104">SYNTAX</span></span>

### <span data-ttu-id="53a9c-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="53a9c-105">ByObject (Default)</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53a9c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="53a9c-106">ByName</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53a9c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="53a9c-107">DESCRIPTION</span></span>
<span data-ttu-id="53a9c-108">Polecenie cmdlet **stop-AzureRmRecoveryServicesAsrJob** zatrzymuje określone zadanie odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="53a9c-108">The **Stop-AzureRmRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="53a9c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="53a9c-109">EXAMPLES</span></span>

### <span data-ttu-id="53a9c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="53a9c-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="53a9c-111">Próbuje zatrzymać określone zadanie i zwraca zaktualizowany obiekt zadania ASR.</span><span class="sxs-lookup"><span data-stu-id="53a9c-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="53a9c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="53a9c-112">PARAMETERS</span></span>

### <span data-ttu-id="53a9c-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="53a9c-113">-Confirm</span></span>
<span data-ttu-id="53a9c-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53a9c-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53a9c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53a9c-115">-DefaultProfile</span></span>
<span data-ttu-id="53a9c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="53a9c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="53a9c-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="53a9c-117">-InputObject</span></span>
<span data-ttu-id="53a9c-118">Obiekt wejściowy: Określ obiekt zadania ASR odpowiadający zadaniu funkcji ASR, który ma zostać zatrzymany</span><span class="sxs-lookup"><span data-stu-id="53a9c-118">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53a9c-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="53a9c-119">-Name</span></span>
<span data-ttu-id="53a9c-120">Określ zadanie ASR, które ma zostać zatrzymane przez nazwę zadania ASR.</span><span class="sxs-lookup"><span data-stu-id="53a9c-120">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="53a9c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53a9c-121">-WhatIf</span></span>
<span data-ttu-id="53a9c-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53a9c-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53a9c-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="53a9c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53a9c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53a9c-124">CommonParameters</span></span>
<span data-ttu-id="53a9c-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53a9c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53a9c-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53a9c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53a9c-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53a9c-127">INPUTS</span></span>

### <span data-ttu-id="53a9c-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="53a9c-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="53a9c-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="53a9c-129">OUTPUTS</span></span>

### <span data-ttu-id="53a9c-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="53a9c-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="53a9c-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="53a9c-131">NOTES</span></span>

## <span data-ttu-id="53a9c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53a9c-132">RELATED LINKS</span></span>

[<span data-ttu-id="53a9c-133">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="53a9c-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="53a9c-134">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="53a9c-134">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="53a9c-135">Życiorys — AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="53a9c-135">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)
