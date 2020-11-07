---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restart-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: c53cc7b410f0898af7a643babef1781433cbd120
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708589"
---
# <span data-ttu-id="ef670-101">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="ef670-101">Restart-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="ef670-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ef670-102">SYNOPSIS</span></span>
<span data-ttu-id="ef670-103">Ponowne uruchamianie zadania odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="ef670-103">Restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="ef670-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ef670-104">SYNTAX</span></span>

### <span data-ttu-id="ef670-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ef670-105">ByObject (Default)</span></span>
```
Restart-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef670-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ef670-106">ByName</span></span>
```
Restart-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef670-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ef670-107">DESCRIPTION</span></span>
<span data-ttu-id="ef670-108">Polecenie cmdlet **restart-AzRecoveryServicesAsrJob** powoduje ponowne uruchomienie zadania odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="ef670-108">The **Restart-AzRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="ef670-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ef670-109">EXAMPLES</span></span>

### <span data-ttu-id="ef670-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ef670-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="ef670-111">Powoduje ponowne uruchomienie określonego zadania ASR i zwraca zaktualizowany obiekt zadania ASR zadania ASR.</span><span class="sxs-lookup"><span data-stu-id="ef670-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="ef670-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ef670-112">PARAMETERS</span></span>

### <span data-ttu-id="ef670-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef670-113">-DefaultProfile</span></span>
<span data-ttu-id="ef670-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ef670-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ef670-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ef670-115">-InputObject</span></span>
<span data-ttu-id="ef670-116">Obiekt wejściowy do polecenia cmdlet: obiekt zadania ASR odpowiadający zadaniu ASR do ponownego uruchomienia</span><span class="sxs-lookup"><span data-stu-id="ef670-116">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>


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

### <span data-ttu-id="ef670-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ef670-117">-Name</span></span>
<span data-ttu-id="ef670-118">Określ zadanie według nazwy.</span><span class="sxs-lookup"><span data-stu-id="ef670-118">Specify the job by name.</span></span>

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

### <span data-ttu-id="ef670-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ef670-119">-Confirm</span></span>
<span data-ttu-id="ef670-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef670-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef670-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef670-121">-WhatIf</span></span>
<span data-ttu-id="ef670-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef670-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef670-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ef670-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef670-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef670-124">CommonParameters</span></span>
<span data-ttu-id="ef670-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef670-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef670-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef670-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef670-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef670-127">INPUTS</span></span>

### <span data-ttu-id="ef670-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ef670-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ef670-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ef670-129">OUTPUTS</span></span>

### <span data-ttu-id="ef670-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ef670-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ef670-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ef670-131">NOTES</span></span>

## <span data-ttu-id="ef670-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef670-132">RELATED LINKS</span></span>

[<span data-ttu-id="ef670-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="ef670-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="ef670-134">Życiorys — AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="ef670-134">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="ef670-135">Zatrzymaj — AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="ef670-135">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
