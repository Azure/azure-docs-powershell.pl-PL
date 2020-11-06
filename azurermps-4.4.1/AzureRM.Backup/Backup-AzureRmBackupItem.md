---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9FF4F649-F50C-4C27-842F-1CD6C5BC7A2B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
ms.openlocfilehash: 1cb5ccf56a2ef6888231ca81df0e352f5d505e7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527738"
---
# <span data-ttu-id="9ffcc-101">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="9ffcc-101">Backup-AzureRmBackupItem</span></span>

## <span data-ttu-id="9ffcc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ffcc-102">SYNOPSIS</span></span>
<span data-ttu-id="9ffcc-103">Rozpoczyna tworzenie kopii zapasowej elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="9ffcc-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ffcc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ffcc-104">SYNTAX</span></span>

```
Backup-AzureRmBackupItem [-Item] <AzureRMBackupItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ffcc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9ffcc-105">DESCRIPTION</span></span>
<span data-ttu-id="9ffcc-106">Polecenie cmdlet **Backup-AzureRmBackupItem** uruchamia wykonywanie kopii zapasowej chronionego elementu kopii zapasowej platformy Azure, który nie jest powiązany z harmonogramem kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="9ffcc-106">The **Backup-AzureRmBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="9ffcc-107">Możesz wykonać wstępną kopię zapasową bezpośrednio po włączeniu ochrony lub po uruchomieniu kopii zapasowej po niepowodzenia zaplanowanej kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="9ffcc-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>

<span data-ttu-id="9ffcc-108">Jeśli jest uruchomione istniejące zadanie kopii zapasowej, to polecenie cmdlet kończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="9ffcc-108">If an existing backup job is running, this cmdlet fails.</span></span>

## <span data-ttu-id="9ffcc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ffcc-109">EXAMPLES</span></span>

### <span data-ttu-id="9ffcc-110">Przykład 1: Rozpoczynanie tworzenia kopii zapasowej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="9ffcc-110">Example 1: Start to back up a virtual machine</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container | Backup-AzureRmBackupItem
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
```

<span data-ttu-id="9ffcc-111">Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="9ffcc-111">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="9ffcc-112">Polecenie zapisuje ten obiekt w zmiennej $Vault.</span><span class="sxs-lookup"><span data-stu-id="9ffcc-112">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="9ffcc-113">Drugie polecenie pobiera kontener o określonej nazwie w magazynie w $Vault przy użyciu Get-AzureRmBackupContainer polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ffcc-113">The second command gets a container that has the specified name in the vault in $Vault by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="9ffcc-114">Polecenie zapisuje ten obiekt w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="9ffcc-114">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="9ffcc-115">Ostatnie polecenie pobiera elementy kopii zapasowej w $Container przy użyciu Get-AzureRmBackupItem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ffcc-115">The last command gets the backup items in $Container by using the Get-AzureRmBackupItem cmdlet.</span></span>
<span data-ttu-id="9ffcc-116">Polecenie przekazuje elementy do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="9ffcc-116">The command passes the items to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9ffcc-117">Bieżące polecenie cmdlet rozpoczyna wykonywanie kopii zapasowej maszyny wirtualnej w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="9ffcc-117">The current cmdlet starts backing up the virtual machine in the container.</span></span>

## <span data-ttu-id="9ffcc-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ffcc-118">PARAMETERS</span></span>

### <span data-ttu-id="9ffcc-119">-Item</span><span class="sxs-lookup"><span data-stu-id="9ffcc-119">-Item</span></span>
<span data-ttu-id="9ffcc-120">Określa element kopii zapasowej, dla którego to polecenie cmdlet rozpoczyna operację tworzenia kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="9ffcc-120">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

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

### <span data-ttu-id="9ffcc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ffcc-121">-DefaultProfile</span></span>
<span data-ttu-id="9ffcc-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9ffcc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ffcc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ffcc-123">CommonParameters</span></span>
<span data-ttu-id="9ffcc-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ffcc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ffcc-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ffcc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ffcc-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ffcc-126">INPUTS</span></span>

### <span data-ttu-id="9ffcc-127">AzureRMBackupItem</span><span class="sxs-lookup"><span data-stu-id="9ffcc-127">AzureRMBackupItem</span></span>

## <span data-ttu-id="9ffcc-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ffcc-128">OUTPUTS</span></span>

### <span data-ttu-id="9ffcc-129">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="9ffcc-129">AzureRmBackupJob</span></span>

## <span data-ttu-id="9ffcc-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ffcc-130">NOTES</span></span>

## <span data-ttu-id="9ffcc-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ffcc-131">RELATED LINKS</span></span>

[<span data-ttu-id="9ffcc-132">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="9ffcc-132">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="9ffcc-133">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="9ffcc-133">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="9ffcc-134">Restore-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="9ffcc-134">Restore-AzureRmBackupItem</span></span>](./Restore-AzureRmBackupItem.md)


