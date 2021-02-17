---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 580f5fd7dc85857bff7257847806bb15dc646ad3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191378"
---
# <span data-ttu-id="a3ec8-101">Get-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a3ec8-101">Get-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="a3ec8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3ec8-102">SYNOPSIS</span></span>
<span data-ttu-id="a3ec8-103">To polecenie spowoduje pobranie wszystkich elementów, które można chronić, w określonym kontenerze lub we wszystkich zarejestrowanych kontenerach.</span><span class="sxs-lookup"><span data-stu-id="a3ec8-103">This command will retrieve all protectable items within a certain container or across all registered containers.</span></span> <span data-ttu-id="a3ec8-104">Będzie się on składał ze wszystkich elementów hierarchii aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a3ec8-104">It will consist of all the elements of the hierarchy of the application.</span></span> <span data-ttu-id="a3ec8-105">Zwraca db i ich jednostki górnej warstwy, takie jak Instance, AvailabilityGroup itp.</span><span class="sxs-lookup"><span data-stu-id="a3ec8-105">Returns DBs and their upper tier entities like Instance, AvailabilityGroup etc.</span></span>

## <span data-ttu-id="a3ec8-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a3ec8-106">SYNTAX</span></span>

### <span data-ttu-id="a3ec8-107">NoFilterParamSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a3ec8-107">NoFilterParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3ec8-108">FilterParamSet</span><span class="sxs-lookup"><span data-stu-id="a3ec8-108">FilterParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [[-ItemType] <ProtectableItemType>] [-Name <String>] [-ServerName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3ec8-109">IdParamSet</span><span class="sxs-lookup"><span data-stu-id="a3ec8-109">IdParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [-ParentID] <String> [[-ItemType] <ProtectableItemType>]
 [-Name <String>] [-ServerName <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3ec8-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="a3ec8-110">DESCRIPTION</span></span>
<span data-ttu-id="a3ec8-111">Polecenie **cmdlet Get-AzRecoveryServicesBackupProtectableItem** pobiera listę elementów, które można chronić, w kontenerze oraz stan ochrony elementów.</span><span class="sxs-lookup"><span data-stu-id="a3ec8-111">The **Get-AzRecoveryServicesBackupProtectableItem** cmdlet gets the list of protectable items in a container and the protection status of the items.</span></span>
<span data-ttu-id="a3ec8-112">Kontener zarejestrowany w magazynie usług Azure Recovery Services może mieć co najmniej jeden element, który może być chroniony.</span><span class="sxs-lookup"><span data-stu-id="a3ec8-112">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>

## <span data-ttu-id="a3ec8-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a3ec8-113">EXAMPLES</span></span>

### <span data-ttu-id="a3ec8-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a3ec8-114">Example 1</span></span>
```
PS C:\> $Vault = Get-AzRecoveryServicesVault -Name "MyRecoveryVault"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer -Status Registered -VaultId $Vault.Id
PS C:\> $Item = Get-AzRecoveryServicesBackupProtectableItem -Container $Container -ItemType "SQLInstance" -WorkloadType "MSSQL" -VaultId $Vault.ID
```

<span data-ttu-id="a3ec8-115">Pierwsze polecenie pobiera kontener typu MSSQL, a następnie przechowuje go w $Container zmienną.</span><span class="sxs-lookup"><span data-stu-id="a3ec8-115">The first command gets the container of type MSSQL, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="a3ec8-116">Drugie polecenie pobiera element z ochroną kopii zapasowej $Container, a następnie przechowuje go w $Item danych.</span><span class="sxs-lookup"><span data-stu-id="a3ec8-116">The second command gets the Backup protectable item in $Container, and then stores it in the $Item variable.</span></span>

## <span data-ttu-id="a3ec8-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3ec8-117">PARAMETERS</span></span>

### <span data-ttu-id="a3ec8-118">— Kontener</span><span class="sxs-lookup"><span data-stu-id="a3ec8-118">-Container</span></span>
<span data-ttu-id="a3ec8-119">Kontener, w którym znajduje się element</span><span class="sxs-lookup"><span data-stu-id="a3ec8-119">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3ec8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3ec8-120">-DefaultProfile</span></span>
<span data-ttu-id="a3ec8-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3ec8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3ec8-122">-ItemType</span><span class="sxs-lookup"><span data-stu-id="a3ec8-122">-ItemType</span></span>
<span data-ttu-id="a3ec8-123">Określa typ elementu, który można chronić.</span><span class="sxs-lookup"><span data-stu-id="a3ec8-123">Specifies the type of protectable item.</span></span> <span data-ttu-id="a3ec8-124">Odpowiednie wartości: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span><span class="sxs-lookup"><span data-stu-id="a3ec8-124">Applicable values: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemType
Parameter Sets: FilterParamSet, IdParamSet
Aliases:
Accepted values: SQLDataBase, SQLInstance, SQLAvailabilityGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3ec8-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a3ec8-125">-Name</span></span>
<span data-ttu-id="a3ec8-126">Określa nazwę bazy danych, wystąpienia lub grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="a3ec8-126">Specifies the name of the Database, Instance or AvailabilityGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterParamSet, IdParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3ec8-127">- ParentID</span><span class="sxs-lookup"><span data-stu-id="a3ec8-127">-ParentID</span></span>
<span data-ttu-id="a3ec8-128">Określono identyfikator ARM wystąpienia lub ag.</span><span class="sxs-lookup"><span data-stu-id="a3ec8-128">Specified the ARM ID of an Instance or AG.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3ec8-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a3ec8-129">-ServerName</span></span>
<span data-ttu-id="a3ec8-130">Określa nazwę serwera, do którego należy element.</span><span class="sxs-lookup"><span data-stu-id="a3ec8-130">Specifies the name of the server to which the item belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterParamSet, IdParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3ec8-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a3ec8-131">-VaultId</span></span>
<span data-ttu-id="a3ec8-132">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a3ec8-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a3ec8-133">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="a3ec8-133">-WorkloadType</span></span>
<span data-ttu-id="a3ec8-134">Typ obciążenia zasobu.</span><span class="sxs-lookup"><span data-stu-id="a3ec8-134">Workload type of the resource.</span></span> <span data-ttu-id="a3ec8-135">Aktualnie obsługiwane wartości to AzureVM, WindowsServer, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="a3ec8-135">The current supported values are  AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:
Accepted values: AzureVM, WindowsServer, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3ec8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3ec8-136">CommonParameters</span></span>
<span data-ttu-id="a3ec8-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3ec8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3ec8-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3ec8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3ec8-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3ec8-139">INPUTS</span></span>

### <span data-ttu-id="a3ec8-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="a3ec8-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="a3ec8-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a3ec8-141">System.String</span></span>

## <span data-ttu-id="a3ec8-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3ec8-142">OUTPUTS</span></span>

### <span data-ttu-id="a3ec8-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.ProtectableItemBase</span><span class="sxs-lookup"><span data-stu-id="a3ec8-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span></span>

## <span data-ttu-id="a3ec8-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a3ec8-144">NOTES</span></span>

## <span data-ttu-id="a3ec8-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3ec8-145">RELATED LINKS</span></span>
