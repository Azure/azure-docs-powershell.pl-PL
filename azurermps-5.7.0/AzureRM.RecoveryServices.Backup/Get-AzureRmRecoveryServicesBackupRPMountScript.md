---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: 0f3f0292b4f348207bf80d5e04c63dc45be69fa3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526709"
---
# <span data-ttu-id="7a296-101">Get-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="7a296-101">Get-AzureRmRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="7a296-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a296-102">SYNOPSIS</span></span>
<span data-ttu-id="7a296-103">Umożliwia pobranie skryptu w celu zainstalowania wszystkich plików punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="7a296-103">Downloads a script to mount all the files of the recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a296-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a296-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a296-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7a296-105">DESCRIPTION</span></span>
<span data-ttu-id="7a296-106">Polecenie cmdlet Get-AzureRmRecoveryServicesBackupRPMountScript Pobiera skrypt instalujący woluminy punktu odzyskiwania na komputerze, na którym jest uruchomiony.</span><span class="sxs-lookup"><span data-stu-id="7a296-106">The Get-AzureRmRecoveryServicesBackupRPMountScript cmdlet downloads a script which mounts the volumes of the recovery point on the machine where it is run.</span></span>

## <span data-ttu-id="7a296-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a296-107">EXAMPLES</span></span>

### <span data-ttu-id="7a296-108">Przykład 1: Instalowanie punktu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="7a296-108">Example 1: Mount a recovery point</span></span>
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

<span data-ttu-id="7a296-109">Po uruchomieniu skryptu spowoduje to zainstalowanie plików punktu odzyskiwania $rp \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="7a296-109">When the script is run, it will mount the files of the recovery point $rp\[0\]</span></span>

## <span data-ttu-id="7a296-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a296-110">PARAMETERS</span></span>

### <span data-ttu-id="7a296-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a296-111">-DefaultProfile</span></span>
<span data-ttu-id="7a296-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a296-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a296-113">-Path</span><span class="sxs-lookup"><span data-stu-id="7a296-113">-Path</span></span>
<span data-ttu-id="7a296-114">Lokalizacja, w której plik ma zostać pobrany w przypadku odzyskiwania plików.</span><span class="sxs-lookup"><span data-stu-id="7a296-114">Location where the file should be downloaded in the case of file recovery.</span></span> <span data-ttu-id="7a296-115">Jeśli nie podano ścieżki, plik skryptu zostanie pobrany w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="7a296-115">If -Path is not provided, the script file will be downloaded in the current directory.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a296-116">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="7a296-116">-RecoveryPoint</span></span>
<span data-ttu-id="7a296-117">Obiekt punktu odzyskiwania do przywrócenia</span><span class="sxs-lookup"><span data-stu-id="7a296-117">Recovery point object to be restored</span></span>

```yaml
Type: RecoveryPointBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a296-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7a296-118">-Confirm</span></span>
<span data-ttu-id="7a296-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a296-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a296-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a296-120">-WhatIf</span></span>
<span data-ttu-id="7a296-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a296-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a296-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7a296-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a296-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a296-123">CommonParameters</span></span>
<span data-ttu-id="7a296-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a296-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a296-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a296-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a296-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a296-126">INPUTS</span></span>

### <span data-ttu-id="7a296-127">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="7a296-127">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="7a296-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a296-128">OUTPUTS</span></span>

### <span data-ttu-id="7a296-129">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RPMountScriptDetails</span><span class="sxs-lookup"><span data-stu-id="7a296-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RPMountScriptDetails</span></span>

## <span data-ttu-id="7a296-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a296-130">NOTES</span></span>

## <span data-ttu-id="7a296-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a296-131">RELATED LINKS</span></span>

