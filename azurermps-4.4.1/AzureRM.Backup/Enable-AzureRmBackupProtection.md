---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: DD150A2C-27D5-4119-9B43-FAB82F9F7D5B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
ms.openlocfilehash: c479869cb150633ca926542552fab2aa7dc80b90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527721"
---
# <span data-ttu-id="40f2d-101">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="40f2d-101">Enable-AzureRmBackupProtection</span></span>

## <span data-ttu-id="40f2d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="40f2d-102">SYNOPSIS</span></span>
<span data-ttu-id="40f2d-103">Kojarzy element z zasadami ochrony kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="40f2d-103">Associates an item with an Azure Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40f2d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="40f2d-104">SYNTAX</span></span>

```
Enable-AzureRmBackupProtection -Policy <AzureRMBackupProtectionPolicy>
 [-Item] <AzureRMBackupContainerContextObject> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40f2d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="40f2d-105">DESCRIPTION</span></span>
<span data-ttu-id="40f2d-106">Polecenie cmdlet **enable-AzureRmBackupProtection** kojarzy element z zasadami ochrony kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="40f2d-106">The **Enable-AzureRmBackupProtection** cmdlet associates an item with an Azure Backup protection policy.</span></span>
<span data-ttu-id="40f2d-107">Aby włączyć zasady ochrony, musisz najpierw mieć istniejący element kopii zapasowej i istniejące zasady.</span><span class="sxs-lookup"><span data-stu-id="40f2d-107">To enable a protection policy, you must first have an existing backup item and an existing policy.</span></span>
<span data-ttu-id="40f2d-108">Oba muszą należeć do tego samego magazynu kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="40f2d-108">Both must belong to the same Backup vault.</span></span>
<span data-ttu-id="40f2d-109">Harmonogram wykonywania kopii zapasowych wykonuje pełną kopię początkową elementu oraz kopię przyrostową kolejnych kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="40f2d-109">The backup schedule does the full initial copy for the item and the incremental copy for the subsequent backups.</span></span>

## <span data-ttu-id="40f2d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="40f2d-110">EXAMPLES</span></span>

### <span data-ttu-id="40f2d-111">Przykład 1: Włączanie ochrony na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="40f2d-111">Example 1: Enable protection on an Azure virtual machine</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Policy = Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered | Get-AzureRmBackupItem | Enable-AzureRmBackupProtection -Policy $Policy
WorkloadName    Operation        Status          StartTime              EndTime
------------    ---------        ------          ---------              -------
co03-vm         ConfigureBackup  Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
```

<span data-ttu-id="40f2d-112">Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="40f2d-112">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="40f2d-113">Polecenie zapisuje ten obiekt w zmiennej $Vault.</span><span class="sxs-lookup"><span data-stu-id="40f2d-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="40f2d-114">Drugie polecenie pobiera zasady ochrony kopii zapasowej o nazwie DefaultPolicy dla magazynu w $Vault.</span><span class="sxs-lookup"><span data-stu-id="40f2d-114">The second command gets the Backup protection policy named DefaultPolicy for the vault in $Vault.</span></span>
<span data-ttu-id="40f2d-115">Polecenie zapisuje ten obiekt w zmiennej $Policy.</span><span class="sxs-lookup"><span data-stu-id="40f2d-115">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="40f2d-116">W poleceniu ostatnim użyto operatora potoku do przekazania wartości z jednego polecenia cmdlet do następnego.</span><span class="sxs-lookup"><span data-stu-id="40f2d-116">The final command uses the pipeline operator to pass values from one cmdlet to the next.</span></span>
<span data-ttu-id="40f2d-117">Na podstawie polecenia cmdlet Get-AzureRmBackupContainer jest pobierany kontener.</span><span class="sxs-lookup"><span data-stu-id="40f2d-117">It gets a container, by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="40f2d-118">Polecenie pobiera element kopii zapasowej z tego kontenera przy użyciu Get-AzureRmBackupItem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40f2d-118">The command gets the backup item from that container by using the Get-AzureRmBackupItem cmdlet.</span></span>
<span data-ttu-id="40f2d-119">Bieżące polecenie cmdlet umożliwia przechowywanie zasad przechowywanych w $Policy elementu, które polecenie przekazuje do tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40f2d-119">The current cmdlet enables the policy stored in $Policy for the item that the command passes to that cmdlet.</span></span>

## <span data-ttu-id="40f2d-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40f2d-120">PARAMETERS</span></span>

### <span data-ttu-id="40f2d-121">-Item</span><span class="sxs-lookup"><span data-stu-id="40f2d-121">-Item</span></span>
<span data-ttu-id="40f2d-122">Określa element kopii zapasowej, dla którego to polecenie cmdlet włącza ochronę.</span><span class="sxs-lookup"><span data-stu-id="40f2d-122">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="40f2d-123">Aby uzyskać **AzureRmBackupItem** , użyj polecenia cmdlet Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="40f2d-123">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainerContextObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40f2d-124">-Policy</span><span class="sxs-lookup"><span data-stu-id="40f2d-124">-Policy</span></span>
<span data-ttu-id="40f2d-125">Określa zasady ochrony, które to polecenie cmdlet kojarzy z elementem.</span><span class="sxs-lookup"><span data-stu-id="40f2d-125">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="40f2d-126">Aby uzyskać obiekt **AzureRmBackupProtectionPolicy** , użyj polecenia cmdlet Get-AzureRmBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="40f2d-126">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f2d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40f2d-127">-DefaultProfile</span></span>
<span data-ttu-id="40f2d-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="40f2d-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40f2d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40f2d-129">CommonParameters</span></span>
<span data-ttu-id="40f2d-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40f2d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40f2d-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40f2d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40f2d-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40f2d-132">INPUTS</span></span>

### <span data-ttu-id="40f2d-133">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="40f2d-133">AzureRmBackupItem</span></span>

## <span data-ttu-id="40f2d-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="40f2d-134">OUTPUTS</span></span>

### <span data-ttu-id="40f2d-135">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="40f2d-135">AzureRmBackupJob</span></span>

## <span data-ttu-id="40f2d-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="40f2d-136">NOTES</span></span>

## <span data-ttu-id="40f2d-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40f2d-137">RELATED LINKS</span></span>

[<span data-ttu-id="40f2d-138">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="40f2d-138">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="40f2d-139">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="40f2d-139">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="40f2d-140">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="40f2d-140">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)


