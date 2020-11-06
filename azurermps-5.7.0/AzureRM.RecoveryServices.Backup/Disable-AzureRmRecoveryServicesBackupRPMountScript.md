---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/disable-azurermrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: bfcd198cd629c9b5f1cd37d3d144bc810a6f4b37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526733"
---
# <span data-ttu-id="eee3c-101">Disable-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="eee3c-101">Disable-AzureRmRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="eee3c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eee3c-102">SYNOPSIS</span></span>
<span data-ttu-id="eee3c-103">Odinstalowuje wszystkie pliki punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="eee3c-103">Dismounts all the files of the recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eee3c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eee3c-104">SYNTAX</span></span>

```
Disable-AzureRmRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eee3c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eee3c-105">DESCRIPTION</span></span>
<span data-ttu-id="eee3c-106">Polecenie cmdlet Disable-AzureRmRecoveryServicesBackupRPMountScript Odinstalowuje pliki punktu odzyskiwania, które zostały zainstalowane wcześniej za pomocą Get-AzureRmRecoveryServicesBackupRPMountScript polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eee3c-106">The Disable-AzureRmRecoveryServicesBackupRPMountScript cmdlet dismounts the files of the recovery point which were mounted earlier using the Get-AzureRmRecoveryServicesBackupRPMountScript cmdlet.</span></span>

## <span data-ttu-id="eee3c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eee3c-107">EXAMPLES</span></span>

### <span data-ttu-id="eee3c-108">Przykład 1: Odinstalowywanie punktu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="eee3c-108">Example 1: Dismount a recovery point</span></span>
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

When the script is run, it will mount the files of the recovery point $rp[0]

After the relevant files are copied, then you remove the files of the recovery point by running the disable cmdlet

PS C:\> Disable-AzureRmRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]
```

## <span data-ttu-id="eee3c-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eee3c-109">PARAMETERS</span></span>

### <span data-ttu-id="eee3c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eee3c-110">-DefaultProfile</span></span>
<span data-ttu-id="eee3c-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eee3c-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eee3c-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eee3c-112">-PassThru</span></span>
<span data-ttu-id="eee3c-113">Zwraca punkt odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="eee3c-113">Return the recovery point.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eee3c-114">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="eee3c-114">-RecoveryPoint</span></span>
<span data-ttu-id="eee3c-115">Obiekt punktu odzyskiwania do przywrócenia</span><span class="sxs-lookup"><span data-stu-id="eee3c-115">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="eee3c-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eee3c-116">-Confirm</span></span>
<span data-ttu-id="eee3c-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eee3c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eee3c-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eee3c-118">-WhatIf</span></span>
<span data-ttu-id="eee3c-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eee3c-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eee3c-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eee3c-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eee3c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eee3c-121">CommonParameters</span></span>
<span data-ttu-id="eee3c-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eee3c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eee3c-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eee3c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eee3c-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eee3c-124">INPUTS</span></span>

### <span data-ttu-id="eee3c-125">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="eee3c-125">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="eee3c-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eee3c-126">OUTPUTS</span></span>

### <span data-ttu-id="eee3c-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="eee3c-127">System.Object</span></span>

## <span data-ttu-id="eee3c-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eee3c-128">NOTES</span></span>

## <span data-ttu-id="eee3c-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eee3c-129">RELATED LINKS</span></span>

