---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9FF4F649-F50C-4C27-842F-1CD6C5BC7A2B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/backup-azurermbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
ms.openlocfilehash: e87ab3ec04378dc97e144d2b444ee5398ff4f4f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551403"
---
# <span data-ttu-id="3cffd-101">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="3cffd-101">Backup-AzureRmBackupItem</span></span>

## <span data-ttu-id="3cffd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3cffd-102">SYNOPSIS</span></span>
<span data-ttu-id="3cffd-103">Rozpoczyna tworzenie kopii zapasowej elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="3cffd-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cffd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3cffd-104">SYNTAX</span></span>

```
Backup-AzureRmBackupItem [-Item] <AzureRMBackupItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3cffd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3cffd-105">DESCRIPTION</span></span>
<span data-ttu-id="3cffd-106">Polecenie cmdlet **Backup-AzureRmBackupItem** uruchamia wykonywanie kopii zapasowej chronionego elementu kopii zapasowej platformy Azure, który nie jest powiązany z harmonogramem kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="3cffd-106">The **Backup-AzureRmBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="3cffd-107">Możesz wykonać wstępną kopię zapasową bezpośrednio po włączeniu ochrony lub po uruchomieniu kopii zapasowej po niepowodzenia zaplanowanej kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="3cffd-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>
<span data-ttu-id="3cffd-108">Jeśli jest uruchomione istniejące zadanie kopii zapasowej, to polecenie cmdlet kończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="3cffd-108">If an existing backup job is running, this cmdlet fails.</span></span>

## <span data-ttu-id="3cffd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3cffd-109">EXAMPLES</span></span>

### <span data-ttu-id="3cffd-110">Przykład 1: Rozpoczynanie tworzenia kopii zapasowej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="3cffd-110">Example 1: Start to back up a virtual machine</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container | Backup-AzureRmBackupItem
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
```

<span data-ttu-id="3cffd-111">Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="3cffd-111">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="3cffd-112">Polecenie zapisuje ten obiekt w zmiennej $Vault.</span><span class="sxs-lookup"><span data-stu-id="3cffd-112">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="3cffd-113">Drugie polecenie pobiera kontener o określonej nazwie w magazynie w $Vault przy użyciu Get-AzureRmBackupContainer polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cffd-113">The second command gets a container that has the specified name in the vault in $Vault by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="3cffd-114">Polecenie zapisuje ten obiekt w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="3cffd-114">The command stores that object in the $Container variable.</span></span>
<span data-ttu-id="3cffd-115">Ostatnie polecenie pobiera elementy kopii zapasowej w $Container przy użyciu Get-AzureRmBackupItem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cffd-115">The last command gets the backup items in $Container by using the Get-AzureRmBackupItem cmdlet.</span></span>
<span data-ttu-id="3cffd-116">Polecenie przekazuje elementy do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="3cffd-116">The command passes the items to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3cffd-117">Bieżące polecenie cmdlet rozpoczyna wykonywanie kopii zapasowej maszyny wirtualnej w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="3cffd-117">The current cmdlet starts backing up the virtual machine in the container.</span></span>

## <span data-ttu-id="3cffd-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3cffd-118">PARAMETERS</span></span>

### <span data-ttu-id="3cffd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cffd-119">-DefaultProfile</span></span>
<span data-ttu-id="3cffd-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3cffd-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3cffd-121">-Item</span><span class="sxs-lookup"><span data-stu-id="3cffd-121">-Item</span></span>
<span data-ttu-id="3cffd-122">Określa element kopii zapasowej, dla którego to polecenie cmdlet rozpoczyna operację tworzenia kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="3cffd-122">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cffd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cffd-123">CommonParameters</span></span>
<span data-ttu-id="3cffd-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cffd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cffd-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cffd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cffd-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3cffd-126">INPUTS</span></span>

### <span data-ttu-id="3cffd-127">Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupItem</span><span class="sxs-lookup"><span data-stu-id="3cffd-127">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem</span></span>
<span data-ttu-id="3cffd-128">Parametry: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3cffd-128">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="3cffd-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3cffd-129">OUTPUTS</span></span>

### <span data-ttu-id="3cffd-130">Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="3cffd-130">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="3cffd-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3cffd-131">NOTES</span></span>

## <span data-ttu-id="3cffd-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3cffd-132">RELATED LINKS</span></span>

[<span data-ttu-id="3cffd-133">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="3cffd-133">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="3cffd-134">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="3cffd-134">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="3cffd-135">Restore-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="3cffd-135">Restore-AzureRmBackupItem</span></span>](./Restore-AzureRmBackupItem.md)


