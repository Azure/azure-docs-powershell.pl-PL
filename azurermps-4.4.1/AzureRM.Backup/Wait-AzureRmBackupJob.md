---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: C5126E20-0A93-4ACE-8297-F1E8E17BEF53
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
ms.openlocfilehash: 6ee1319881b200b3fcae56e433f81460bfc90274
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551944"
---
# <span data-ttu-id="6741a-101">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="6741a-101">Wait-AzureRmBackupJob</span></span>

## <span data-ttu-id="6741a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6741a-102">SYNOPSIS</span></span>
<span data-ttu-id="6741a-103">Oczekuje na zakończenie zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="6741a-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6741a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6741a-104">SYNTAX</span></span>

```
Wait-AzureRmBackupJob -Job <Object> [-TimeOut <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6741a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6741a-105">DESCRIPTION</span></span>
<span data-ttu-id="6741a-106">Polecenie cmdlet **wait-AzureRmBackupJob** oczekuje na zakończenie zadania kopii zapasowej Azure.</span><span class="sxs-lookup"><span data-stu-id="6741a-106">The **Wait-AzureRmBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="6741a-107">Zadania tworzenia kopii zapasowej mogą trwać długo.</span><span class="sxs-lookup"><span data-stu-id="6741a-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="6741a-108">Jeśli uruchomisz zadanie kopii zapasowej w ramach skryptu, możesz wymusić, że skrypt będzie czekał na zakończenie zadania, zanim przełączy się do innych zadań.</span><span class="sxs-lookup"><span data-stu-id="6741a-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>

<span data-ttu-id="6741a-109">Skrypt zawierający to polecenie cmdlet może być łatwiejszy niż ten, który sonduje usługę kopii zapasowej dla stanu zadania.</span><span class="sxs-lookup"><span data-stu-id="6741a-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>

## <span data-ttu-id="6741a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6741a-110">EXAMPLES</span></span>

## <span data-ttu-id="6741a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6741a-111">PARAMETERS</span></span>

### <span data-ttu-id="6741a-112">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="6741a-112">-Job</span></span>
<span data-ttu-id="6741a-113">Określa zadanie, które zostanie anulowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6741a-113">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="6741a-114">Aby uzyskać obiekt **AzureRmBackupJob** , użyj polecenia cmdlet Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="6741a-114">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6741a-115">-TimeOut</span><span class="sxs-lookup"><span data-stu-id="6741a-115">-TimeOut</span></span>
<span data-ttu-id="6741a-116">Określa maksymalny czas (w sekundach) oczekiwania na zakończenie zadania.</span><span class="sxs-lookup"><span data-stu-id="6741a-116">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="6741a-117">Zalecamy określenie wartości limitu czasu.</span><span class="sxs-lookup"><span data-stu-id="6741a-117">We recommend that you specify a time-out value.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6741a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6741a-118">-DefaultProfile</span></span>
<span data-ttu-id="6741a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6741a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6741a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6741a-120">CommonParameters</span></span>
<span data-ttu-id="6741a-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6741a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6741a-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6741a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6741a-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6741a-123">INPUTS</span></span>

### <span data-ttu-id="6741a-124">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="6741a-124">AzureRmBackupJob</span></span>

## <span data-ttu-id="6741a-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6741a-125">OUTPUTS</span></span>

### <span data-ttu-id="6741a-126">AzureRmBackupJob[]</span><span class="sxs-lookup"><span data-stu-id="6741a-126">AzureRmBackupJob[]</span></span>

## <span data-ttu-id="6741a-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6741a-127">NOTES</span></span>

## <span data-ttu-id="6741a-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6741a-128">RELATED LINKS</span></span>

[<span data-ttu-id="6741a-129">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="6741a-129">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="6741a-130">Zatrzymaj — AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="6741a-130">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)


