---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/backup-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: a7451855f62a9e0eab63936107d8431342badfb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551664"
---
# <span data-ttu-id="0b76f-101">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="0b76f-101">Backup-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="0b76f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0b76f-102">SYNOPSIS</span></span>
<span data-ttu-id="0b76f-103">Rozpoczyna tworzenie kopii zapasowej elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="0b76f-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b76f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0b76f-104">SYNTAX</span></span>

```
Backup-AzureRmRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b76f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0b76f-105">DESCRIPTION</span></span>
<span data-ttu-id="0b76f-106">Polecenie cmdlet **Backup-AzureRmRecoveryServicesBackupItem** uruchamia wykonywanie kopii zapasowej chronionego elementu kopii zapasowej platformy Azure, który nie jest powiązany z harmonogramem kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="0b76f-106">The **Backup-AzureRmRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="0b76f-107">Możesz wykonać wstępną kopię zapasową bezpośrednio po włączeniu ochrony lub po uruchomieniu kopii zapasowej po niepowodzenia zaplanowanej kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="0b76f-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>

<span data-ttu-id="0b76f-108">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="0b76f-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="0b76f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0b76f-109">EXAMPLES</span></span>

### <span data-ttu-id="0b76f-110">Przykład 1. Rozpoczynanie wykonywania kopii zapasowej elementu kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="0b76f-110">Example 1: Start a backup for a Backup item</span></span>
```
PS C:\> $NamedContainer = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "pstestv2vm1" 
PS C:\> $Item = Get-AzureRmRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM 
PS C:\> $Job = Backup-AzureRmRecoveryServicesItem -Item $Item
Operation        Status               StartTime            EndTime                   JOBID                           
------------     ---------            ------               ---------                 -------                                         
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="0b76f-111">Pierwsze polecenie pobiera kontener kopii zapasowych typu AzureVM o nazwie pstestv2vm1, a następnie zapisuje go w zmiennej $NamedContainer.</span><span class="sxs-lookup"><span data-stu-id="0b76f-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>

<span data-ttu-id="0b76f-112">Drugie polecenie pobiera element kopii zapasowej odpowiadający kontenerowi w $NamedContainer, a następnie zapisuje go w zmiennej $Item.</span><span class="sxs-lookup"><span data-stu-id="0b76f-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>

<span data-ttu-id="0b76f-113">Ostatnie polecenie wyzwala zadanie kopii zapasowej dla elementu kopii zapasowej w $Item.</span><span class="sxs-lookup"><span data-stu-id="0b76f-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="0b76f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0b76f-114">PARAMETERS</span></span>

### <span data-ttu-id="0b76f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b76f-115">-DefaultProfile</span></span>
<span data-ttu-id="0b76f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0b76f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b76f-117">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="0b76f-117">-ExpiryDateTimeUTC</span></span>
<span data-ttu-id="0b76f-118">Określa czas wygaśnięcia jako obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="0b76f-118">Specifies an expiry time as a **DateTime** object.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b76f-119">-Item</span><span class="sxs-lookup"><span data-stu-id="0b76f-119">-Item</span></span>
<span data-ttu-id="0b76f-120">Określa element kopii zapasowej, dla którego to polecenie cmdlet rozpoczyna operację tworzenia kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="0b76f-120">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: ItemBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b76f-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0b76f-121">-Confirm</span></span>
<span data-ttu-id="0b76f-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b76f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b76f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b76f-123">-WhatIf</span></span>
<span data-ttu-id="0b76f-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b76f-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b76f-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0b76f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b76f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b76f-126">CommonParameters</span></span>
<span data-ttu-id="0b76f-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b76f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b76f-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b76f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b76f-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b76f-129">INPUTS</span></span>

### <span data-ttu-id="0b76f-130">Zmiennej</span><span class="sxs-lookup"><span data-stu-id="0b76f-130">DateTime</span></span>
<span data-ttu-id="0b76f-131">Parametr "ExpiryDateTimeUTC" akceptuje wartość typu "DateTime" z procesu</span><span class="sxs-lookup"><span data-stu-id="0b76f-131">Parameter 'ExpiryDateTimeUTC' accepts value of type 'DateTime' from the pipeline</span></span>

### <span data-ttu-id="0b76f-132">ItemBase</span><span class="sxs-lookup"><span data-stu-id="0b76f-132">ItemBase</span></span>
<span data-ttu-id="0b76f-133">Parametr "element" akceptuje wartość typu "ItemBase" z potoku</span><span class="sxs-lookup"><span data-stu-id="0b76f-133">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="0b76f-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0b76f-134">OUTPUTS</span></span>

### <span data-ttu-id="0b76f-135">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="0b76f-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="0b76f-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0b76f-136">NOTES</span></span>

## <span data-ttu-id="0b76f-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b76f-137">RELATED LINKS</span></span>

[<span data-ttu-id="0b76f-138">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="0b76f-138">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="0b76f-139">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="0b76f-139">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="0b76f-140">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="0b76f-140">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


