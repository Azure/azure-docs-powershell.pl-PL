---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 44C5AF58-ADC1-4BC6-9771-3FD8F0480106
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/stop-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
ms.openlocfilehash: 800b5c6e04e0842113db7fb3494815bcd97ebfb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541943"
---
# <span data-ttu-id="50c38-101">Stop-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="50c38-101">Stop-AzureRmBackupJob</span></span>

## <span data-ttu-id="50c38-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="50c38-102">SYNOPSIS</span></span>
<span data-ttu-id="50c38-103">Anuluje istniejące zadanie kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="50c38-103">Cancels an existing Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50c38-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="50c38-104">SYNTAX</span></span>

### <span data-ttu-id="50c38-105">IdFiltersSet</span><span class="sxs-lookup"><span data-stu-id="50c38-105">IdFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Vault <AzureRMBackupVault> -JobID <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50c38-106">JobFiltersSet</span><span class="sxs-lookup"><span data-stu-id="50c38-106">JobFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50c38-107">Opis</span><span class="sxs-lookup"><span data-stu-id="50c38-107">DESCRIPTION</span></span>
<span data-ttu-id="50c38-108">Polecenie cmdlet **stop-AzureRmBackupJob** anuluje istniejące zadanie kopii zapasowej Azure.</span><span class="sxs-lookup"><span data-stu-id="50c38-108">The **Stop-AzureRmBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="50c38-109">Za pomocą tego parametru można zatrzymać zadanie, które trwa zbyt długo i blokuje inne działania.</span><span class="sxs-lookup"><span data-stu-id="50c38-109">Use this parameter to stop a job that takes too long and blocks other activities.</span></span>
<span data-ttu-id="50c38-110">Możesz anulować tylko następujące typy zadań:</span><span class="sxs-lookup"><span data-stu-id="50c38-110">You can cancel only the following types of jobs:</span></span> 
- <span data-ttu-id="50c38-111">Wykonania</span><span class="sxs-lookup"><span data-stu-id="50c38-111">Backup</span></span>
- <span data-ttu-id="50c38-112">Przywrócenie</span><span class="sxs-lookup"><span data-stu-id="50c38-112">Restore</span></span>

## <span data-ttu-id="50c38-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="50c38-113">EXAMPLES</span></span>

### <span data-ttu-id="50c38-114">Przykład 1: zatrzymanie zadania kopii zapasowej przy użyciu identyfikatora zadania</span><span class="sxs-lookup"><span data-stu-id="50c38-114">Example 1: Stop a backup job by using a job ID</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Job = Get-AzureRmBackupJob -Vault $Vault -Operation Backup
PS C:\> Stop-AzureRmBackupJob -Vault $Vault -JobID $Job.InstanceId
```

<span data-ttu-id="50c38-115">Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="50c38-115">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="50c38-116">Polecenie zapisuje ten obiekt w zmiennej $Vault.</span><span class="sxs-lookup"><span data-stu-id="50c38-116">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="50c38-117">Drugie polecenie pobiera zadanie kopii zapasowej z magazynu w $Vault przy użyciu polecenia cmdlet **Get-AzureRmBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="50c38-117">The second command gets a backup job from the vault in $Vault by using the **Get-AzureRmBackupJob** cmdlet.</span></span>
<span data-ttu-id="50c38-118">Polecenie zapisuje zadanie w zmiennej $Job.</span><span class="sxs-lookup"><span data-stu-id="50c38-118">The command stores the job in the $Job variable.</span></span>
<span data-ttu-id="50c38-119">W tym przykładzie istnieje tylko jedna operacja wykonywania kopii zapasowej w określonym magazynie.</span><span class="sxs-lookup"><span data-stu-id="50c38-119">In this example, there is only one backup operation in the specified vault.</span></span>
<span data-ttu-id="50c38-120">Polecenie ostatnie zatrzymuje zadanie o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="50c38-120">The final command stops the job that has the specified ID.</span></span>

### <span data-ttu-id="50c38-121">Przykład 2: zatrzymanie wszystkich operacji przywracania</span><span class="sxs-lookup"><span data-stu-id="50c38-121">Example 2: Stop all Restore operations</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Operation Restore | Stop-AzureRmBackupJob
```

<span data-ttu-id="50c38-122">To polecenie pobiera wszystkie operacje przywracania w magazynie w $Vault, a następnie przekazuje je do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="50c38-122">This command gets all the restore operations in the vault in $Vault, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="50c38-123">Bieżące polecenie cmdlet zatrzymuje każde zadanie.</span><span class="sxs-lookup"><span data-stu-id="50c38-123">The current cmdlet stops each job.</span></span>

## <span data-ttu-id="50c38-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="50c38-124">PARAMETERS</span></span>

### <span data-ttu-id="50c38-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50c38-125">-DefaultProfile</span></span>
<span data-ttu-id="50c38-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="50c38-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50c38-127">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="50c38-127">-Job</span></span>
<span data-ttu-id="50c38-128">Określa zadanie, które zostanie anulowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50c38-128">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="50c38-129">Aby uzyskać obiekt **AzureRmBackupJob** , użyj polecenia cmdlet Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="50c38-129">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="50c38-130">-JobID</span><span class="sxs-lookup"><span data-stu-id="50c38-130">-JobID</span></span>
<span data-ttu-id="50c38-131">Określa zadanie, które zostanie anulowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50c38-131">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="50c38-132">Aby uzyskać obiekt **AzureRmBackupJob** , użyj polecenia cmdlet Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="50c38-132">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="50c38-133">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="50c38-133">-Vault</span></span>
<span data-ttu-id="50c38-134">Określa magazyn kopii zapasowych, w którym to polecenie cmdlet anuluje zadanie.</span><span class="sxs-lookup"><span data-stu-id="50c38-134">Specifies the Backup vault in which this cmdlet cancels a job.</span></span>
<span data-ttu-id="50c38-135">Aby uzyskać obiekt **AzureRmBackupVault** , użyj polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="50c38-135">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="50c38-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50c38-136">CommonParameters</span></span>
<span data-ttu-id="50c38-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50c38-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50c38-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50c38-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50c38-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50c38-139">INPUTS</span></span>

### <span data-ttu-id="50c38-140">Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="50c38-140">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>
<span data-ttu-id="50c38-141">Parametry: zadanie (ByValue)</span><span class="sxs-lookup"><span data-stu-id="50c38-141">Parameters: Job (ByValue)</span></span>

## <span data-ttu-id="50c38-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="50c38-142">OUTPUTS</span></span>

### <span data-ttu-id="50c38-143">System. void</span><span class="sxs-lookup"><span data-stu-id="50c38-143">System.Void</span></span>

## <span data-ttu-id="50c38-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="50c38-144">NOTES</span></span>

## <span data-ttu-id="50c38-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50c38-145">RELATED LINKS</span></span>

[<span data-ttu-id="50c38-146">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="50c38-146">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="50c38-147">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="50c38-147">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="50c38-148">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="50c38-148">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


