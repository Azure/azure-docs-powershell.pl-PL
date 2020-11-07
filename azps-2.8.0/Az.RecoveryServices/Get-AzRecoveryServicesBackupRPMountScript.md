---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: 6301c621de4399509c70271eb318983e91ebd121
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872679"
---
# <span data-ttu-id="8c430-101">Get-AzRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="8c430-101">Get-AzRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="8c430-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8c430-102">SYNOPSIS</span></span>
<span data-ttu-id="8c430-103">Umożliwia pobranie skryptu w celu zainstalowania wszystkich plików punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="8c430-103">Downloads a script to mount all the files of the recovery point.</span></span>

## <span data-ttu-id="8c430-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8c430-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [[-Path] <String>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c430-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8c430-105">DESCRIPTION</span></span>
<span data-ttu-id="8c430-106">Polecenie cmdlet Get-AzRecoveryServicesBackupRPMountScript Pobiera skrypt instalujący woluminy punktu odzyskiwania na komputerze, na którym jest uruchomiony.</span><span class="sxs-lookup"><span data-stu-id="8c430-106">The Get-AzRecoveryServicesBackupRPMountScript cmdlet downloads a script which mounts the volumes of the recovery point on the machine where it is run.</span></span>

## <span data-ttu-id="8c430-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8c430-107">EXAMPLES</span></span>

### <span data-ttu-id="8c430-108">Przykład 1: Instalowanie punktu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="8c430-108">Example 1: Mount a recovery point</span></span>
```
PS C:\> $namedContainer = Get-AzRecoveryServicesBackupContainer  -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM"
PS C:\> $backupitem = Get-AzRecoveryServicesBackupItem -Container $namedContainer  -WorkloadType "AzureVM"
PS C:\> $startDate = (Get-Date).AddDays(-7)
PS C:\> $endDate = Get-Date
PS C:\> $rp = Get-AzRecoveryServicesBackupRecoveryPoint -Item $backupitem -StartDate $startdate.ToUniversalTime() -EndDate $enddate.ToUniversalTime()

To mount files of the latest recovery point, obtain the script by

PS C:\> Get-AzRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]

OsType  Password        Filename
------  --------        --------
Windows e3632984e51f496 V2VM_wus2_8287309959960546283_451516692429_cbd6061f7fc543c489f1974d33659fed07a6e0c2e08740.exe
```

<span data-ttu-id="8c430-109">Po uruchomieniu skryptu spowoduje to zainstalowanie plików punktu odzyskiwania $rp \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="8c430-109">When the script is run, it will mount the files of the recovery point $rp\[0\]</span></span>

## <span data-ttu-id="8c430-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8c430-110">PARAMETERS</span></span>

### <span data-ttu-id="8c430-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c430-111">-DefaultProfile</span></span>
<span data-ttu-id="8c430-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c430-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c430-113">-Path</span><span class="sxs-lookup"><span data-stu-id="8c430-113">-Path</span></span>
<span data-ttu-id="8c430-114">Lokalizacja, w której plik ma zostać pobrany w przypadku odzyskiwania plików.</span><span class="sxs-lookup"><span data-stu-id="8c430-114">Location where the file should be downloaded in the case of file recovery.</span></span> <span data-ttu-id="8c430-115">Jeśli nie podano ścieżki, plik skryptu zostanie pobrany w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="8c430-115">If -Path is not provided, the script file will be downloaded in the current directory.</span></span>

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

### <span data-ttu-id="8c430-116">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="8c430-116">-RecoveryPoint</span></span>
<span data-ttu-id="8c430-117">Obiekt punktu odzyskiwania do przywrócenia</span><span class="sxs-lookup"><span data-stu-id="8c430-117">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="8c430-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="8c430-118">-VaultId</span></span>
<span data-ttu-id="8c430-119">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="8c430-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8c430-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8c430-120">-Confirm</span></span>
<span data-ttu-id="8c430-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c430-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c430-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c430-122">-WhatIf</span></span>
<span data-ttu-id="8c430-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c430-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c430-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8c430-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c430-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c430-125">CommonParameters</span></span>
<span data-ttu-id="8c430-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c430-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c430-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c430-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c430-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c430-128">INPUTS</span></span>

### <span data-ttu-id="8c430-129">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="8c430-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

### <span data-ttu-id="8c430-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8c430-130">System.String</span></span>

## <span data-ttu-id="8c430-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8c430-131">OUTPUTS</span></span>

### <span data-ttu-id="8c430-132">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RPMountScriptDetails</span><span class="sxs-lookup"><span data-stu-id="8c430-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RPMountScriptDetails</span></span>

## <span data-ttu-id="8c430-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8c430-133">NOTES</span></span>

## <span data-ttu-id="8c430-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c430-134">RELATED LINKS</span></span>
