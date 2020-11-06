---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: 6caf37bf8e9b4bc11969ff4f1e0e55e7e0d6880c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547352"
---
# <span data-ttu-id="4d106-101">Get-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="4d106-101">Get-AzureRmRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="4d106-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d106-102">SYNOPSIS</span></span>
<span data-ttu-id="4d106-103">Umożliwia pobranie skryptu w celu zainstalowania wszystkich plików punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="4d106-103">Downloads a script to mount all the files of the recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d106-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d106-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [[-Path] <String>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d106-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4d106-105">DESCRIPTION</span></span>
<span data-ttu-id="4d106-106">Polecenie cmdlet Get-AzureRmRecoveryServicesBackupRPMountScript Pobiera skrypt instalujący woluminy punktu odzyskiwania na komputerze, na którym jest uruchomiony.</span><span class="sxs-lookup"><span data-stu-id="4d106-106">The Get-AzureRmRecoveryServicesBackupRPMountScript cmdlet downloads a script which mounts the volumes of the recovery point on the machine where it is run.</span></span>

## <span data-ttu-id="4d106-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d106-107">EXAMPLES</span></span>

### <span data-ttu-id="4d106-108">Przykład 1: Instalowanie punktu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="4d106-108">Example 1: Mount a recovery point</span></span>
```
PS C:\> $namedContainer = Get-AzureRmRecoveryServicesBackupContainer  -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM"
PS C:\> $backupitem = Get-AzureRmRecoveryServicesBackupItem -Container $namedContainer  -WorkloadType "AzureVM"
PS C:\> $startDate = (Get-Date).AddDays(-7)
PS C:\> $endDate = Get-Date
PS C:\> $rp = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $backupitem -StartDate $startdate.ToUniversalTime() -EndDate $enddate.ToUniversalTime()

To mount files of the latest recovery point, obtain the script by

PS C:\> Get-AzureRmRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]

OsType  Password        Filename
------  --------        --------
Windows e3632984e51f496 V2VM_wus2_8287309959960546283_451516692429_cbd6061f7fc543c489f1974d33659fed07a6e0c2e08740.exe
```

<span data-ttu-id="4d106-109">Po uruchomieniu skryptu spowoduje to zainstalowanie plików punktu odzyskiwania $rp \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="4d106-109">When the script is run, it will mount the files of the recovery point $rp\[0\]</span></span>

## <span data-ttu-id="4d106-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d106-110">PARAMETERS</span></span>

### <span data-ttu-id="4d106-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d106-111">-DefaultProfile</span></span>
<span data-ttu-id="4d106-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d106-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d106-113">-Path</span><span class="sxs-lookup"><span data-stu-id="4d106-113">-Path</span></span>
<span data-ttu-id="4d106-114">Lokalizacja, w której plik ma zostać pobrany w przypadku odzyskiwania plików.</span><span class="sxs-lookup"><span data-stu-id="4d106-114">Location where the file should be downloaded in the case of file recovery.</span></span> <span data-ttu-id="4d106-115">Jeśli nie podano ścieżki, plik skryptu zostanie pobrany w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="4d106-115">If -Path is not provided, the script file will be downloaded in the current directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d106-116">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="4d106-116">-RecoveryPoint</span></span>
<span data-ttu-id="4d106-117">Obiekt punktu odzyskiwania do przywrócenia</span><span class="sxs-lookup"><span data-stu-id="4d106-117">Recovery point object to be restored</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d106-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="4d106-118">-VaultId</span></span>
<span data-ttu-id="4d106-119">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="4d106-119">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d106-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4d106-120">-Confirm</span></span>
<span data-ttu-id="4d106-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d106-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d106-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d106-122">-WhatIf</span></span>
<span data-ttu-id="4d106-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d106-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d106-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4d106-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d106-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d106-125">CommonParameters</span></span>
<span data-ttu-id="4d106-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d106-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d106-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d106-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d106-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d106-128">INPUTS</span></span>

### <span data-ttu-id="4d106-129">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="4d106-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="4d106-130">Parametry: RecoveryPoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4d106-130">Parameters: RecoveryPoint (ByValue)</span></span>

### <span data-ttu-id="4d106-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4d106-131">System.String</span></span>
<span data-ttu-id="4d106-132">Parametry: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4d106-132">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="4d106-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d106-133">OUTPUTS</span></span>

### <span data-ttu-id="4d106-134">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RPMountScriptDetails</span><span class="sxs-lookup"><span data-stu-id="4d106-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RPMountScriptDetails</span></span>

## <span data-ttu-id="4d106-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d106-135">NOTES</span></span>

## <span data-ttu-id="4d106-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d106-136">RELATED LINKS</span></span>
