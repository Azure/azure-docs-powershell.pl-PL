---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 44C5AF58-ADC1-4BC6-9771-3FD8F0480106
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
ms.openlocfilehash: d502596b8c5ddde576b5fd22ee31398b2c4e869a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553383"
---
# <span data-ttu-id="8b72b-101">Stop-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="8b72b-101">Stop-AzureRmBackupJob</span></span>

## <span data-ttu-id="8b72b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8b72b-102">SYNOPSIS</span></span>
<span data-ttu-id="8b72b-103">Anuluje istniejące zadanie kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="8b72b-103">Cancels an existing Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b72b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8b72b-104">SYNTAX</span></span>

### <span data-ttu-id="8b72b-105">IdFiltersSet</span><span class="sxs-lookup"><span data-stu-id="8b72b-105">IdFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Vault <AzureRMBackupVault> -JobID <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b72b-106">JobFiltersSet</span><span class="sxs-lookup"><span data-stu-id="8b72b-106">JobFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b72b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8b72b-107">DESCRIPTION</span></span>
<span data-ttu-id="8b72b-108">Polecenie cmdlet **stop-AzureRmBackupJob** anuluje istniejące zadanie kopii zapasowej Azure.</span><span class="sxs-lookup"><span data-stu-id="8b72b-108">The **Stop-AzureRmBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="8b72b-109">Za pomocą tego parametru można zatrzymać zadanie, które trwa zbyt długo i blokuje inne działania.</span><span class="sxs-lookup"><span data-stu-id="8b72b-109">Use this parameter to stop a job that takes too long and blocks other activities.</span></span>

<span data-ttu-id="8b72b-110">Możesz anulować tylko następujące typy zadań:</span><span class="sxs-lookup"><span data-stu-id="8b72b-110">You can cancel only the following types of jobs:</span></span> 

- <span data-ttu-id="8b72b-111">Wykonania</span><span class="sxs-lookup"><span data-stu-id="8b72b-111">Backup</span></span>
- <span data-ttu-id="8b72b-112">Przywrócenie</span><span class="sxs-lookup"><span data-stu-id="8b72b-112">Restore</span></span>

## <span data-ttu-id="8b72b-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8b72b-113">EXAMPLES</span></span>

### <span data-ttu-id="8b72b-114">Przykład 1: zatrzymanie zadania kopii zapasowej przy użyciu identyfikatora zadania</span><span class="sxs-lookup"><span data-stu-id="8b72b-114">Example 1: Stop a backup job by using a job ID</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Job = Get-AzureRmBackupJob -Vault $Vault -Operation Backup
PS C:\> Stop-AzureRmBackupJob -Vault $Vault -JobID $Job.InstanceId
```

<span data-ttu-id="8b72b-115">Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="8b72b-115">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="8b72b-116">Polecenie zapisuje ten obiekt w zmiennej $Vault.</span><span class="sxs-lookup"><span data-stu-id="8b72b-116">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="8b72b-117">Drugie polecenie pobiera zadanie kopii zapasowej z magazynu w $Vault przy użyciu polecenia cmdlet **Get-AzureRmBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="8b72b-117">The second command gets a backup job from the vault in $Vault by using the **Get-AzureRmBackupJob** cmdlet.</span></span>
<span data-ttu-id="8b72b-118">Polecenie zapisuje zadanie w zmiennej $Job.</span><span class="sxs-lookup"><span data-stu-id="8b72b-118">The command stores the job in the $Job variable.</span></span>
<span data-ttu-id="8b72b-119">W tym przykładzie istnieje tylko jedna operacja wykonywania kopii zapasowej w określonym magazynie.</span><span class="sxs-lookup"><span data-stu-id="8b72b-119">In this example, there is only one backup operation in the specified vault.</span></span>

<span data-ttu-id="8b72b-120">Polecenie ostatnie zatrzymuje zadanie o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="8b72b-120">The final command stops the job that has the specified ID.</span></span>

### <span data-ttu-id="8b72b-121">Przykład 2: zatrzymanie wszystkich operacji przywracania</span><span class="sxs-lookup"><span data-stu-id="8b72b-121">Example 2: Stop all Restore operations</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Operation Restore | Stop-AzureRmBackupJob
```

<span data-ttu-id="8b72b-122">To polecenie pobiera wszystkie operacje przywracania w magazynie w $Vault, a następnie przekazuje je do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="8b72b-122">This command gets all the restore operations in the vault in $Vault, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8b72b-123">Bieżące polecenie cmdlet zatrzymuje każde zadanie.</span><span class="sxs-lookup"><span data-stu-id="8b72b-123">The current cmdlet stops each job.</span></span>

## <span data-ttu-id="8b72b-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8b72b-124">PARAMETERS</span></span>

### <span data-ttu-id="8b72b-125">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="8b72b-125">-Job</span></span>
<span data-ttu-id="8b72b-126">Określa zadanie, które zostanie anulowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b72b-126">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="8b72b-127">Aby uzyskać obiekt **AzureRmBackupJob** , użyj polecenia cmdlet Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="8b72b-127">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b72b-128">-JobID</span><span class="sxs-lookup"><span data-stu-id="8b72b-128">-JobID</span></span>
<span data-ttu-id="8b72b-129">Określa zadanie, które zostanie anulowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b72b-129">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="8b72b-130">Aby uzyskać obiekt **AzureRmBackupJob** , użyj polecenia cmdlet Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="8b72b-130">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b72b-131">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="8b72b-131">-Vault</span></span>
<span data-ttu-id="8b72b-132">Określa magazyn kopii zapasowych, w którym to polecenie cmdlet anuluje zadanie.</span><span class="sxs-lookup"><span data-stu-id="8b72b-132">Specifies the Backup vault in which this cmdlet cancels a job.</span></span>
<span data-ttu-id="8b72b-133">Aby uzyskać obiekt **AzureRmBackupVault** , użyj polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="8b72b-133">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b72b-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b72b-134">-DefaultProfile</span></span>
<span data-ttu-id="8b72b-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8b72b-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b72b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b72b-136">CommonParameters</span></span>
<span data-ttu-id="8b72b-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b72b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b72b-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b72b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b72b-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b72b-139">INPUTS</span></span>

### <span data-ttu-id="8b72b-140">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="8b72b-140">AzureRmBackupJob</span></span>

## <span data-ttu-id="8b72b-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8b72b-141">OUTPUTS</span></span>

### <span data-ttu-id="8b72b-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8b72b-142">None</span></span>

## <span data-ttu-id="8b72b-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8b72b-143">NOTES</span></span>

## <span data-ttu-id="8b72b-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b72b-144">RELATED LINKS</span></span>

[<span data-ttu-id="8b72b-145">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="8b72b-145">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="8b72b-146">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="8b72b-146">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="8b72b-147">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="8b72b-147">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


