---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: F3774658-A5E4-40BE-9A85-B33C70BC0A09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
ms.openlocfilehash: abc4bce43c5be267e736cb93e03806cdd802fcb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527122"
---
# <span data-ttu-id="726bc-101">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="726bc-101">Get-AzureRmBackupContainer</span></span>

## <span data-ttu-id="726bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="726bc-102">SYNOPSIS</span></span>
<span data-ttu-id="726bc-103">Pobiera kontenery kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="726bc-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="726bc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="726bc-104">SYNTAX</span></span>

```
Get-AzureRmBackupContainer [-Name <String>] -Type <AzureBackupContainerType>
 [-ManagedResourceGroupName <String>] [-Status <AzureBackupContainerRegistrationStatus>]
 [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="726bc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="726bc-105">DESCRIPTION</span></span>
<span data-ttu-id="726bc-106">Polecenie cmdlet **Get-AzureRmBackupContainer** pobiera kontenery kopii zapasowych Azure.</span><span class="sxs-lookup"><span data-stu-id="726bc-106">The **Get-AzureRmBackupContainer** cmdlet gets Azure Backup containers.</span></span>

<span data-ttu-id="726bc-107">**AzureBackupContainer** hermetyzuje źródła danych, elementy chronione i punkty odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="726bc-107">An **AzureBackupContainer** encapsulates data sources, protected items, and recovery points.</span></span>
<span data-ttu-id="726bc-108">**AzureBackupContainer** może być jednym z następujących:</span><span class="sxs-lookup"><span data-stu-id="726bc-108">An **AzureBackupContainer** can be one of the following:</span></span> 

- <span data-ttu-id="726bc-109">Komputer z systemem Windows Server</span><span class="sxs-lookup"><span data-stu-id="726bc-109">A Windows Server computer</span></span>
- <span data-ttu-id="726bc-110">Serwer programu System Center Data Protection Manager (SCDPM)</span><span class="sxs-lookup"><span data-stu-id="726bc-110">A System Center Data Protection Manager (SCDPM) server</span></span> 
- <span data-ttu-id="726bc-111">Infrastruktura platformy Azure jako maszyna wirtualna usługi (IaaS)</span><span class="sxs-lookup"><span data-stu-id="726bc-111">An Azure infrastructure as a service (IaaS) virtual machine</span></span>

<span data-ttu-id="726bc-112">Zanim kopia zapasowa może utworzyć kopię zapasową źródła danych lub elementu, należy zarejestrować kontener, w którym znajduje się usługa kopii zapasowej Azure.</span><span class="sxs-lookup"><span data-stu-id="726bc-112">Before Backup can back up a data source or item, you must register the container that holds it with the Azure Backup service.</span></span>
<span data-ttu-id="726bc-113">Aby można było wysyłać dane kopii zapasowej do magazynu kopii zapasowych, kontener musi być uwierzytelniony.</span><span class="sxs-lookup"><span data-stu-id="726bc-113">The container must be authenticated to send backup data to the Backup vault.</span></span>
<span data-ttu-id="726bc-114">W przypadku komputerów z systemem Windows Server i serwerów SCDPM Rejestracja odbywa się przy użyciu w pełni kwalifikowanej nazwy domeny serwera.</span><span class="sxs-lookup"><span data-stu-id="726bc-114">For Windows Server computers and SCDPM servers, the registration is held with the fully qualified domain name of the server.</span></span>

## <span data-ttu-id="726bc-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="726bc-115">EXAMPLES</span></span>

### <span data-ttu-id="726bc-116">Przykład 1: wyświetlanie wszystkich serwerów zarejestrowanych w magazynie</span><span class="sxs-lookup"><span data-stu-id="726bc-116">Example 1: View all servers registered to a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type Windows
Name                         Type               Status
----                         ----               ------
SERVER01.CONTOSO.COM          Windows            Registered
SERVER02.CONTOSO.COM          Windows            Registered
```

<span data-ttu-id="726bc-117">Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="726bc-117">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="726bc-118">Polecenie zapisuje ten obiekt w zmiennej $Vault.</span><span class="sxs-lookup"><span data-stu-id="726bc-118">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="726bc-119">Drugie polecenie pobiera wszystkie kontenery typu Windows z magazynu w $Vault.</span><span class="sxs-lookup"><span data-stu-id="726bc-119">The second command gets all containers of type Windows from the vault in $Vault.</span></span>

### <span data-ttu-id="726bc-120">Przykład 2: uzyskiwanie określonego kontenera</span><span class="sxs-lookup"><span data-stu-id="726bc-120">Example 2: Get a specific container</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type SCDPM -Name "DPMSERVER.CONTOSO.COM"
Name                         Type               Status
----                         ----               ------
DPMSERVER.CONTOSO.COM        SCDPM              Registered
```

<span data-ttu-id="726bc-121">To polecenie uzyskuje kontener o nazwie DPMSERVER. CONTOSO.COM.</span><span class="sxs-lookup"><span data-stu-id="726bc-121">This command gets the container named DPMSERVER.CONTOSO.COM.</span></span>
<span data-ttu-id="726bc-122">To polecenie określa magazyn w $Vault i typ kontenera.</span><span class="sxs-lookup"><span data-stu-id="726bc-122">The command specifies the vault in $Vault and the type of container.</span></span>

### <span data-ttu-id="726bc-123">Przykład 3: wyświetlanie wszystkich zarejestrowanych maszyn wirtualnych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="726bc-123">Example 3: View all registered Azure virtual machines</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered 
Name                         Type               Status
----                         ----               ------
co03-vm                      AzureVM            Registered
```

<span data-ttu-id="726bc-124">To polecenie umożliwia pobieranie zarejestrowanych maszyn wirtualnych z magazynu w $Vault.</span><span class="sxs-lookup"><span data-stu-id="726bc-124">This command gets the registered virtual machines from the vault in $Vault.</span></span>

## <span data-ttu-id="726bc-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="726bc-125">PARAMETERS</span></span>

### <span data-ttu-id="726bc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="726bc-126">-DefaultProfile</span></span>
<span data-ttu-id="726bc-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="726bc-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="726bc-128">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="726bc-128">-ManagedResourceGroupName</span></span>
<span data-ttu-id="726bc-129">Określa nazwę grupy zasobów skojarzonej z kontenerem.</span><span class="sxs-lookup"><span data-stu-id="726bc-129">Specifies the name of the resource group associated with the container.</span></span>
<span data-ttu-id="726bc-130">Ta nazwa jest taka sama, jak wartość określona dla parametru *ServiceName* lub *ResourceGroupName* polecenia cmdlet Register-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="726bc-130">This name is the same value that you specified for the *ServiceName* or *ResourceGroupName* parameter of the Register-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726bc-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="726bc-131">-Name</span></span>
<span data-ttu-id="726bc-132">Określa nazwę kontenera, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="726bc-132">Specifies the name of the container that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726bc-133">-Status</span><span class="sxs-lookup"><span data-stu-id="726bc-133">-Status</span></span>
<span data-ttu-id="726bc-134">Określa bieżący stan kontenerów, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="726bc-134">Specifies the current status of the containers that this cmdlet gets.</span></span>
<span data-ttu-id="726bc-135">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="726bc-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="726bc-136">NotRegistered</span><span class="sxs-lookup"><span data-stu-id="726bc-136">NotRegistered</span></span> 
- <span data-ttu-id="726bc-137">Zarejestrować</span><span class="sxs-lookup"><span data-stu-id="726bc-137">Registered</span></span> 
- <span data-ttu-id="726bc-138">Rejestracj</span><span class="sxs-lookup"><span data-stu-id="726bc-138">Registering</span></span>

```yaml
Type: AzureBackupContainerRegistrationStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Registered, Registering, NotRegistered

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726bc-139">-Type</span><span class="sxs-lookup"><span data-stu-id="726bc-139">-Type</span></span>
<span data-ttu-id="726bc-140">Określa typy kontenerów, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="726bc-140">Specifies the type of containers that this cmdlet gets.</span></span>

```yaml
Type: AzureBackupContainerType
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, SCDPM, AzureVM, AzureBackupServer, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726bc-141">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="726bc-141">-Vault</span></span>
<span data-ttu-id="726bc-142">Określa magazyn kopii zapasowych, z którego to polecenie cmdlet pobiera kontenery.</span><span class="sxs-lookup"><span data-stu-id="726bc-142">Specifies a Backup vault from which this cmdlet gets containers.</span></span>
<span data-ttu-id="726bc-143">Aby uzyskać **AzureRmBackupVault** , użyj polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="726bc-143">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="726bc-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="726bc-144">CommonParameters</span></span>
<span data-ttu-id="726bc-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="726bc-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="726bc-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="726bc-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="726bc-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="726bc-147">INPUTS</span></span>

### <span data-ttu-id="726bc-148">AzureBackupVault</span><span class="sxs-lookup"><span data-stu-id="726bc-148">AzureBackupVault</span></span>

## <span data-ttu-id="726bc-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="726bc-149">OUTPUTS</span></span>

### <span data-ttu-id="726bc-150">AzureBackupContainer</span><span class="sxs-lookup"><span data-stu-id="726bc-150">AzureBackupContainer</span></span>

## <span data-ttu-id="726bc-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="726bc-151">NOTES</span></span>
* <span data-ttu-id="726bc-152">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="726bc-152">None</span></span>

## <span data-ttu-id="726bc-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="726bc-153">RELATED LINKS</span></span>

[<span data-ttu-id="726bc-154">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="726bc-154">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="726bc-155">Rejestr — AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="726bc-155">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)

[<span data-ttu-id="726bc-156">Wyrejestrowanie — AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="726bc-156">Unregister-AzureRmBackupContainer</span></span>](./Unregister-AzureRmBackupContainer.md)


