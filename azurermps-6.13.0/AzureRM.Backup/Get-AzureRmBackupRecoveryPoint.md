---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6778E018-B6CC-468A-823E-3DA047EA6B52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
ms.openlocfilehash: f82abc45a9b78093c13764ab0eb28f2593c7fabb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547628"
---
# <span data-ttu-id="cd632-101">Get-AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="cd632-101">Get-AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="cd632-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd632-102">SYNOPSIS</span></span>
<span data-ttu-id="cd632-103">Pobiera punkty odzyskiwania dla elementu z kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="cd632-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd632-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd632-104">SYNTAX</span></span>

```
Get-AzureRmBackupRecoveryPoint [[-RecoveryPointId] <String>] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd632-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cd632-105">DESCRIPTION</span></span>
<span data-ttu-id="cd632-106">Polecenie cmdlet **Get-AzureRmBackupRecoveryPoint** pobiera punkty odzyskiwania dla kopii zapasowej elementu kopii zapasowej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cd632-106">The **Get-AzureRmBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="cd632-107">Po wykonaniu kopii zapasowej elementu kopia zapasowa przechowuje jeden lub więcej punktów odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="cd632-107">After an item has been backed up, Backup stores one or more recovery points.</span></span>

## <span data-ttu-id="cd632-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd632-108">EXAMPLES</span></span>

### <span data-ttu-id="cd632-109">Przykład 1: uzyskiwanie punktów odzyskiwania dla elementu</span><span class="sxs-lookup"><span data-stu-id="cd632-109">Example 1: Get recovery points for an item</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> Get-AzureRmBackupRecoveryPoint -Item $BackupItem
RecoveryPointId    RecoveryPointType  RecoveryPointTime      ContainerName
---------------    -----------------  -----------------      -------------
15273496567119     AppConsistent      26-Aug-15 12:27:38 PM  iaasvmcontainer;conto02-vm;conto0...
```

<span data-ttu-id="cd632-110">Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="cd632-110">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="cd632-111">Polecenie zapisuje ten obiekt w zmiennej $Vault.</span><span class="sxs-lookup"><span data-stu-id="cd632-111">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="cd632-112">Drugie polecenie pobiera kontener o określonej nazwie w magazynie w $Vault przy użyciu polecenia cmdlet **Get-AzureRmBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="cd632-112">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="cd632-113">Polecenie zapisuje ten obiekt w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="cd632-113">The command stores that object in the $Container variable.</span></span>
<span data-ttu-id="cd632-114">Trzecie polecenie pobiera element kopii zapasowej w kontenerze w $Container przy użyciu polecenia cmdlet **Get-AzureRmBackupItem** .</span><span class="sxs-lookup"><span data-stu-id="cd632-114">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="cd632-115">Polecenie zapisuje ten obiekt w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="cd632-115">The command stores that object in the $BackupItem variable.</span></span>
<span data-ttu-id="cd632-116">Polecenie ostatnie pobiera punkty odzyskiwania dla elementu w $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="cd632-116">The final command gets recovery points for the item in $BackupItem.</span></span>

## <span data-ttu-id="cd632-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd632-117">PARAMETERS</span></span>

### <span data-ttu-id="cd632-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd632-118">-DefaultProfile</span></span>
<span data-ttu-id="cd632-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cd632-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd632-120">-Item</span><span class="sxs-lookup"><span data-stu-id="cd632-120">-Item</span></span>
<span data-ttu-id="cd632-121">Określa element, dla którego to polecenie cmdlet umożliwia pobieranie punktów odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="cd632-121">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="cd632-122">Aby uzyskać **AzureRmBackupItem** , użyj polecenia cmdlet Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="cd632-122">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="cd632-123">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="cd632-123">-RecoveryPointId</span></span>
<span data-ttu-id="cd632-124">Określa identyfikator punktu odzyskiwania, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd632-124">Specifies the ID of a recovery point that this cmdlet gets.</span></span>

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

### <span data-ttu-id="cd632-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd632-125">CommonParameters</span></span>
<span data-ttu-id="cd632-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd632-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd632-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd632-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd632-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd632-128">INPUTS</span></span>

### <span data-ttu-id="cd632-129">Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupItem</span><span class="sxs-lookup"><span data-stu-id="cd632-129">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem</span></span>
<span data-ttu-id="cd632-130">Parametry: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cd632-130">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="cd632-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd632-131">OUTPUTS</span></span>

### <span data-ttu-id="cd632-132">Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="cd632-132">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRecoveryPoint</span></span>

## <span data-ttu-id="cd632-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd632-133">NOTES</span></span>

## <span data-ttu-id="cd632-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd632-134">RELATED LINKS</span></span>

[<span data-ttu-id="cd632-135">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="cd632-135">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="cd632-136">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="cd632-136">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="cd632-137">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="cd632-137">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


