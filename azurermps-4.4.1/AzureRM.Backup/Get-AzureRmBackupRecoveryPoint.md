---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6778E018-B6CC-468A-823E-3DA047EA6B52
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
ms.openlocfilehash: 0a5c5f42f7a6f4755335a5b8827fd2d23e096679
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528289"
---
# <span data-ttu-id="d7d3e-101">Get-AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="d7d3e-101">Get-AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="d7d3e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7d3e-102">SYNOPSIS</span></span>
<span data-ttu-id="d7d3e-103">Pobiera punkty odzyskiwania dla elementu z kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="d7d3e-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7d3e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7d3e-104">SYNTAX</span></span>

```
Get-AzureRmBackupRecoveryPoint [[-RecoveryPointId] <String>] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7d3e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d7d3e-105">DESCRIPTION</span></span>
<span data-ttu-id="d7d3e-106">Polecenie cmdlet **Get-AzureRmBackupRecoveryPoint** pobiera punkty odzyskiwania dla kopii zapasowej elementu kopii zapasowej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d7d3e-106">The **Get-AzureRmBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="d7d3e-107">Po wykonaniu kopii zapasowej elementu kopia zapasowa przechowuje jeden lub więcej punktów odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d7d3e-107">After an item has been backed up, Backup stores one or more recovery points.</span></span>

## <span data-ttu-id="d7d3e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7d3e-108">EXAMPLES</span></span>

### <span data-ttu-id="d7d3e-109">Przykład 1: uzyskiwanie punktów odzyskiwania dla elementu</span><span class="sxs-lookup"><span data-stu-id="d7d3e-109">Example 1: Get recovery points for an item</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> Get-AzureRmBackupRecoveryPoint -Item $BackupItem
RecoveryPointId    RecoveryPointType  RecoveryPointTime      ContainerName
---------------    -----------------  -----------------      -------------
15273496567119     AppConsistent      26-Aug-15 12:27:38 PM  iaasvmcontainer;conto02-vm;conto0...
```

<span data-ttu-id="d7d3e-110">Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="d7d3e-110">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="d7d3e-111">Polecenie zapisuje ten obiekt w zmiennej $Vault.</span><span class="sxs-lookup"><span data-stu-id="d7d3e-111">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="d7d3e-112">Drugie polecenie pobiera kontener o określonej nazwie w magazynie w $Vault przy użyciu polecenia cmdlet **Get-AzureRmBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="d7d3e-112">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="d7d3e-113">Polecenie zapisuje ten obiekt w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="d7d3e-113">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="d7d3e-114">Trzecie polecenie pobiera element kopii zapasowej w kontenerze w $Container przy użyciu polecenia cmdlet **Get-AzureRmBackupItem** .</span><span class="sxs-lookup"><span data-stu-id="d7d3e-114">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="d7d3e-115">Polecenie zapisuje ten obiekt w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="d7d3e-115">The command stores that object in the $BackupItem variable.</span></span>

<span data-ttu-id="d7d3e-116">Polecenie ostatnie pobiera punkty odzyskiwania dla elementu w $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="d7d3e-116">The final command gets recovery points for the item in $BackupItem.</span></span>

## <span data-ttu-id="d7d3e-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7d3e-117">PARAMETERS</span></span>

### <span data-ttu-id="d7d3e-118">-Item</span><span class="sxs-lookup"><span data-stu-id="d7d3e-118">-Item</span></span>
<span data-ttu-id="d7d3e-119">Określa element, dla którego to polecenie cmdlet umożliwia pobieranie punktów odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d7d3e-119">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="d7d3e-120">Aby uzyskać **AzureRmBackupItem** , użyj polecenia cmdlet Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="d7d3e-120">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="d7d3e-121">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="d7d3e-121">-RecoveryPointId</span></span>
<span data-ttu-id="d7d3e-122">Określa identyfikator punktu odzyskiwania, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7d3e-122">Specifies the ID of a recovery point that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d7d3e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7d3e-123">-DefaultProfile</span></span>
<span data-ttu-id="d7d3e-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7d3e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7d3e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7d3e-125">CommonParameters</span></span>
<span data-ttu-id="d7d3e-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7d3e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7d3e-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7d3e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7d3e-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7d3e-128">INPUTS</span></span>

### <span data-ttu-id="d7d3e-129">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="d7d3e-129">AzureRmBackupItem</span></span>

## <span data-ttu-id="d7d3e-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7d3e-130">OUTPUTS</span></span>

### <span data-ttu-id="d7d3e-131">AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="d7d3e-131">AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="d7d3e-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7d3e-132">NOTES</span></span>

## <span data-ttu-id="d7d3e-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7d3e-133">RELATED LINKS</span></span>

[<span data-ttu-id="d7d3e-134">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="d7d3e-134">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="d7d3e-135">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="d7d3e-135">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="d7d3e-136">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="d7d3e-136">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


