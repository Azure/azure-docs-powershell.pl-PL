---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 8A638FB1-F530-4E28-BAAE-5382671092C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
ms.openlocfilehash: f0380a518353c3bc462a8a7b58012871359569a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543943"
---
# <span data-ttu-id="37dcb-101">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="37dcb-101">Get-AzureRmBackupItem</span></span>

## <span data-ttu-id="37dcb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="37dcb-102">SYNOPSIS</span></span>
<span data-ttu-id="37dcb-103">Pobiera elementy pod kontenerem w programie Kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="37dcb-103">Gets the items under a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37dcb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="37dcb-104">SYNTAX</span></span>

```
Get-AzureRmBackupItem [-ProtectionStatus <String>] [-Status <String>] [-Type <String>]
 [-Container] <AzureRMBackupContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37dcb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="37dcb-105">DESCRIPTION</span></span>
<span data-ttu-id="37dcb-106">Polecenie cmdlet **Get-AzureRmBackupItem** Pobiera elementy w kontenerze w usłudze Kopia zapasowa Azure oraz stan ochrony elementów.</span><span class="sxs-lookup"><span data-stu-id="37dcb-106">The **Get-AzureRmBackupItem** cmdlet gets the items in a container in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="37dcb-107">Włączanie elementów do ochrony przy użyciu Enable-AzureRmBackupProtection polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37dcb-107">Enable items for protection by using the Enable-AzureRmBackupProtection cmdlet.</span></span>
<span data-ttu-id="37dcb-108">Kontener zarejestrowany w magazynie kopii zapasowych może zawierać jeden lub więcej elementów, które mogą być chronione.</span><span class="sxs-lookup"><span data-stu-id="37dcb-108">A container that is registered to a Backup vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="37dcb-109">W przypadku maszyn wirtualnych platformy Azure w kontenerze maszyny wirtualnej może być tylko jedna pozycja.</span><span class="sxs-lookup"><span data-stu-id="37dcb-109">For Azure virtual machines, there can be only one item in the virtual machine container.</span></span>

## <span data-ttu-id="37dcb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="37dcb-110">EXAMPLES</span></span>

### <span data-ttu-id="37dcb-111">Przykład 1. Pobieranie elementów w kontenerze</span><span class="sxs-lookup"><span data-stu-id="37dcb-111">Example 1: Get the items in a container</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container
Name                    ProtectionStatus       DataSourceStatus       RecoveryPointsCount    ProtectionPolicyName
----                    ----------------       ----------------       -------------------    --------------------
co03-vm                 NotProtected                                  0
```

<span data-ttu-id="37dcb-112">Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="37dcb-112">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="37dcb-113">Polecenie zapisuje ten obiekt w zmiennej $Vault.</span><span class="sxs-lookup"><span data-stu-id="37dcb-113">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="37dcb-114">Drugie polecenie pobiera kontener o określonej nazwie w magazynie w $Vault przy użyciu polecenia cmdlet **Get-AzureRmBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="37dcb-114">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="37dcb-115">Polecenie zapisuje ten obiekt w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="37dcb-115">The command stores that object in the $Container variable.</span></span>
<span data-ttu-id="37dcb-116">Polecenie ostatnie Pobiera element kopii zapasowej w kontenerze w $Container.</span><span class="sxs-lookup"><span data-stu-id="37dcb-116">The final command gets the backup item in the container in $Container.</span></span>

### <span data-ttu-id="37dcb-117">Przykład 2: wyświetlanie wszystkich właściwości elementu</span><span class="sxs-lookup"><span data-stu-id="37dcb-117">Example 2: View all properties for an item</span></span>
```
PS C:\>Get-AzureRmBackupItem -Container $Container | Select-Object -Property *
Name                 : co03-vm
DataSourceStatus     : 
ProtectionStatus     : NotProtected
Type                 : AzureVM
ProtectionPolicyName : 
ProtectionPolicyId   : 
RecoveryPointsCount  : 0
ItemName             : iaasvmcontainer;co03-vm;co03-vm
ContainerType        : AzureVM
ContainerUniqueName  : iaasvmcontainer;co03-vm;co03-vm
ResourceGroupName    : resourcegroup02
ResourceName         : vault03
Location             : southeastasia
```

<span data-ttu-id="37dcb-118">To polecenie pobiera element kopii zapasowej w kontenerze w $Container, a następnie przekazuje go do Select-Object polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37dcb-118">This command gets the backup item in the container in $Container, and then passes it to the Select-Object cmdlet.</span></span>
<span data-ttu-id="37dcb-119">To polecenie cmdlet zwraca wszystkie właściwości elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="37dcb-119">That cmdlet returns all properties of the backup item.</span></span>
<span data-ttu-id="37dcb-120">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Select-Object` .</span><span class="sxs-lookup"><span data-stu-id="37dcb-120">For more information, type `Get-Help Select-Object`.</span></span>

## <span data-ttu-id="37dcb-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="37dcb-121">PARAMETERS</span></span>

### <span data-ttu-id="37dcb-122">-Kontener</span><span class="sxs-lookup"><span data-stu-id="37dcb-122">-Container</span></span>
<span data-ttu-id="37dcb-123">Określa obiekt kontenera, dla którego to polecenie cmdlet pobiera elementy kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="37dcb-123">Specifies a container object for which this cmdlet gets backup items.</span></span>
<span data-ttu-id="37dcb-124">Aby uzyskać **AzureRmBackupContainer** , użyj polecenia cmdlet Get-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="37dcb-124">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37dcb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37dcb-125">-DefaultProfile</span></span>
<span data-ttu-id="37dcb-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="37dcb-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37dcb-127">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="37dcb-127">-ProtectionStatus</span></span>
<span data-ttu-id="37dcb-128">Określa ogólny stan ochrony elementu w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="37dcb-128">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="37dcb-129">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="37dcb-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37dcb-130">Chroniony</span><span class="sxs-lookup"><span data-stu-id="37dcb-130">Protected</span></span> 
- <span data-ttu-id="37dcb-131">Aktywn</span><span class="sxs-lookup"><span data-stu-id="37dcb-131">Protecting</span></span>  
- <span data-ttu-id="37dcb-132">NotProtected</span><span class="sxs-lookup"><span data-stu-id="37dcb-132">NotProtected</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Protected, Protecting, NotProtected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37dcb-133">-Status</span><span class="sxs-lookup"><span data-stu-id="37dcb-133">-Status</span></span>
<span data-ttu-id="37dcb-134">Określa stan kopii zapasowej elementu.</span><span class="sxs-lookup"><span data-stu-id="37dcb-134">Specifies the backup status for an item.</span></span>
<span data-ttu-id="37dcb-135">Dopuszczalne wartości tego parametru to: IRPending, protected, ProtectionError i ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="37dcb-135">The acceptable values for this parameter are: IRPending, Protected, ProtectionError, and ProtectionStopped.</span></span>
<span data-ttu-id="37dcb-136">Jeśli parametr *ProtectionStatus* ma wartość protected, możesz filtrować elementy za pomocą wartości parametru *status* .</span><span class="sxs-lookup"><span data-stu-id="37dcb-136">If the *ProtectionStatus* parameter has the value Protected, you can use the *Status* parameter value to filter items.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IRPending, ProtectionStopped, ProtectionError, Protected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37dcb-137">-Type</span><span class="sxs-lookup"><span data-stu-id="37dcb-137">-Type</span></span>
<span data-ttu-id="37dcb-138">Określa typ elementu, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37dcb-138">Specifies the type of item that this cmdlet gets.</span></span>
<span data-ttu-id="37dcb-139">Obecnie jedyną obsługiwaną wartością jest AzureVM.</span><span class="sxs-lookup"><span data-stu-id="37dcb-139">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37dcb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37dcb-140">CommonParameters</span></span>
<span data-ttu-id="37dcb-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37dcb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37dcb-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37dcb-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37dcb-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37dcb-143">INPUTS</span></span>

### <span data-ttu-id="37dcb-144">Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupContainer</span><span class="sxs-lookup"><span data-stu-id="37dcb-144">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer</span></span>
<span data-ttu-id="37dcb-145">Parametry: kontener (ByValue)</span><span class="sxs-lookup"><span data-stu-id="37dcb-145">Parameters: Container (ByValue)</span></span>

## <span data-ttu-id="37dcb-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="37dcb-146">OUTPUTS</span></span>

### <span data-ttu-id="37dcb-147">Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupItem</span><span class="sxs-lookup"><span data-stu-id="37dcb-147">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem</span></span>

## <span data-ttu-id="37dcb-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="37dcb-148">NOTES</span></span>

## <span data-ttu-id="37dcb-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37dcb-149">RELATED LINKS</span></span>

[<span data-ttu-id="37dcb-150">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="37dcb-150">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="37dcb-151">Disable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="37dcb-151">Disable-AzureRmBackupProtection</span></span>](./Disable-AzureRmBackupProtection.md)

[<span data-ttu-id="37dcb-152">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="37dcb-152">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="37dcb-153">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="37dcb-153">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="37dcb-154">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="37dcb-154">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="37dcb-155">Restore-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="37dcb-155">Restore-AzureRmBackupItem</span></span>](./Restore-AzureRmBackupItem.md)


