---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: add399ca208cdcd1f1b4395523f8df43875ff451
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232954"
---
# <span data-ttu-id="8bf5e-101">Get-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="8bf5e-101">Get-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="8bf5e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8bf5e-102">SYNOPSIS</span></span>
<span data-ttu-id="8bf5e-103">To polecenie spowoduje pobranie wszystkich elementów podlegających ochronie w określonym kontenerze lub we wszystkich zarejestrowanych kontenerach.</span><span class="sxs-lookup"><span data-stu-id="8bf5e-103">This command will retrieve all protectable items within a certain container or across all registered containers.</span></span> <span data-ttu-id="8bf5e-104">Będzie on zawierać wszystkie elementy hierarchii aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8bf5e-104">It will consist of all the elements of the hierarchy of the application.</span></span> <span data-ttu-id="8bf5e-105">Zwraca DBs i ich wyższe jednostki, takie jak instancja, Availability itd.</span><span class="sxs-lookup"><span data-stu-id="8bf5e-105">Returns DBs and their upper tier entities like Instance, AvailabilityGroup etc.</span></span>

## <span data-ttu-id="8bf5e-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8bf5e-106">SYNTAX</span></span>

### <span data-ttu-id="8bf5e-107">NoFilterParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8bf5e-107">NoFilterParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8bf5e-108">FilterParamSet</span><span class="sxs-lookup"><span data-stu-id="8bf5e-108">FilterParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [[-ItemType] <ProtectableItemType>] [-Name <String>] [-ServerName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8bf5e-109">IdParamSet</span><span class="sxs-lookup"><span data-stu-id="8bf5e-109">IdParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [-ParentID] <String> [[-ItemType] <ProtectableItemType>]
 [-Name <String>] [-ServerName <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8bf5e-110">Opis</span><span class="sxs-lookup"><span data-stu-id="8bf5e-110">DESCRIPTION</span></span>
<span data-ttu-id="8bf5e-111">Polecenie cmdlet **Get-AzRecoveryServicesBackupProtectableItem** pobiera listę elementów z możliwością ochrony w kontenerze oraz stan ochrony elementów.</span><span class="sxs-lookup"><span data-stu-id="8bf5e-111">The **Get-AzRecoveryServicesBackupProtectableItem** cmdlet gets the list of protectable items in a container and the protection status of the items.</span></span>
<span data-ttu-id="8bf5e-112">Kontener zarejestrowany w magazynie usług odzyskiwania Azure może zawierać jeden lub więcej elementów, które mogą być chronione.</span><span class="sxs-lookup"><span data-stu-id="8bf5e-112">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>

## <span data-ttu-id="8bf5e-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8bf5e-113">EXAMPLES</span></span>

### <span data-ttu-id="8bf5e-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8bf5e-114">Example 1</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType MSSQL -Status Registered
PS C:\> $Item = Get-AzRecoveryServicesProtectableItem -Container $Container -ItemType "SQLDatabase" -VaultId $vault.ID
```

<span data-ttu-id="8bf5e-115">Pierwsze polecenie uzyskuje kontener typu MSSQL, a następnie zapisuje go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="8bf5e-115">The first command gets the container of type MSSQL, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="8bf5e-116">Drugie polecenie pobiera element kopii zapasowej z ochroną w $Container, a następnie zapisuje go w zmiennej $Item.</span><span class="sxs-lookup"><span data-stu-id="8bf5e-116">The second command gets the Backup protectable item in $Container, and then stores it in the $Item variable.</span></span>

## <span data-ttu-id="8bf5e-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8bf5e-117">PARAMETERS</span></span>

### <span data-ttu-id="8bf5e-118">-Kontener</span><span class="sxs-lookup"><span data-stu-id="8bf5e-118">-Container</span></span>
<span data-ttu-id="8bf5e-119">Kontener, w którym znajduje się element</span><span class="sxs-lookup"><span data-stu-id="8bf5e-119">Container where the item resides</span></span>

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

### <span data-ttu-id="8bf5e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bf5e-120">-DefaultProfile</span></span>
<span data-ttu-id="8bf5e-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8bf5e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bf5e-122">-ItemType</span><span class="sxs-lookup"><span data-stu-id="8bf5e-122">-ItemType</span></span>
<span data-ttu-id="8bf5e-123">Określa typ elementu do ochrony.</span><span class="sxs-lookup"><span data-stu-id="8bf5e-123">Specifies the type of protectable item.</span></span> <span data-ttu-id="8bf5e-124">Odpowiednie wartości: (SQLDatabase, SQLInstance, sqlavailabilitys).</span><span class="sxs-lookup"><span data-stu-id="8bf5e-124">Applicable values: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span></span>

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

### <span data-ttu-id="8bf5e-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8bf5e-125">-Name</span></span>
<span data-ttu-id="8bf5e-126">Określa nazwę bazy danych, wystąpienia lub funkcji Availability.</span><span class="sxs-lookup"><span data-stu-id="8bf5e-126">Specifies the name of the Database, Instance or AvailabilityGroup.</span></span>

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

### <span data-ttu-id="8bf5e-127">-ParentID</span><span class="sxs-lookup"><span data-stu-id="8bf5e-127">-ParentID</span></span>
<span data-ttu-id="8bf5e-128">Określono identyfikator ARM wystąpienia lub AG.</span><span class="sxs-lookup"><span data-stu-id="8bf5e-128">Specified the ARM ID of an Instance or AG.</span></span>

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

### <span data-ttu-id="8bf5e-129">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="8bf5e-129">-ServerName</span></span>
<span data-ttu-id="8bf5e-130">Określa nazwę serwera, do którego należy dany element.</span><span class="sxs-lookup"><span data-stu-id="8bf5e-130">Specifies the name of the server to which the item belongs.</span></span>

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

### <span data-ttu-id="8bf5e-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="8bf5e-131">-VaultId</span></span>
<span data-ttu-id="8bf5e-132">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="8bf5e-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8bf5e-133">-Obciążenia</span><span class="sxs-lookup"><span data-stu-id="8bf5e-133">-WorkloadType</span></span>
<span data-ttu-id="8bf5e-134">Typ obciążenia pracą zasobu.</span><span class="sxs-lookup"><span data-stu-id="8bf5e-134">Workload type of the resource.</span></span> <span data-ttu-id="8bf5e-135">Obecnie obsługiwane wartości to AzureVM, WindowsServer, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="8bf5e-135">The current supported values are  AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="8bf5e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bf5e-136">CommonParameters</span></span>
<span data-ttu-id="8bf5e-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bf5e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bf5e-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8bf5e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bf5e-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8bf5e-139">INPUTS</span></span>

### <span data-ttu-id="8bf5e-140">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="8bf5e-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="8bf5e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8bf5e-141">System.String</span></span>

## <span data-ttu-id="8bf5e-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8bf5e-142">OUTPUTS</span></span>

### <span data-ttu-id="8bf5e-143">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ProtectableItemBase</span><span class="sxs-lookup"><span data-stu-id="8bf5e-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span></span>

## <span data-ttu-id="8bf5e-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8bf5e-144">NOTES</span></span>

## <span data-ttu-id="8bf5e-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8bf5e-145">RELATED LINKS</span></span>
