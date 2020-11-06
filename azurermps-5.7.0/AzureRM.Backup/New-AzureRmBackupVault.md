---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 015E3BC9-C535-4EA2-8A30-C728385DBFF8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
ms.openlocfilehash: 77c2df1ec61b42aaded458bea564cf6c953c90ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550663"
---
# <span data-ttu-id="ef295-101">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="ef295-101">New-AzureRmBackupVault</span></span>

## <span data-ttu-id="ef295-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ef295-102">SYNOPSIS</span></span>
<span data-ttu-id="ef295-103">Tworzy magazyn kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="ef295-103">Creates a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef295-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ef295-104">SYNTAX</span></span>

```
New-AzureRmBackupVault [-ResourceGroupName] <String> [-Name] <String> [-Region] <String>
 [[-Storage] <AzureBackupVaultStorageType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef295-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ef295-105">DESCRIPTION</span></span>
<span data-ttu-id="ef295-106">Polecenie cmdlet **New-AzureRmBackupVault** tworzy magazyn kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ef295-106">The **New-AzureRmBackupVault** cmdlet creates an Azure Backup vault.</span></span>
<span data-ttu-id="ef295-107">To polecenie cmdlet zwraca obiekt **AzureRmBackupVault** , który działa jako odwołanie do jednostki magazynu.</span><span class="sxs-lookup"><span data-stu-id="ef295-107">This cmdlet returns an **AzureRmBackupVault** object that acts as a reference to the vault entity.</span></span>

## <span data-ttu-id="ef295-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ef295-108">EXAMPLES</span></span>

### <span data-ttu-id="ef295-109">Przykład 1. Tworzenie magazynu kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="ef295-109">Example 1: Create a backup vault</span></span>
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup01" -Name "Vault03" -Region "westus"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup01/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

<span data-ttu-id="ef295-110">To polecenie tworzy magazyn kopii zapasowych Azure o nazwie Vault03.</span><span class="sxs-lookup"><span data-stu-id="ef295-110">This command creates an Azure Backup vault named Vault03.</span></span>
<span data-ttu-id="ef295-111">Magazyn znajduje się w grupie zasobów o nazwie ResourceGroup01 w zachodnim regionie Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="ef295-111">The vault is in the resource group named ResourceGroup01 in the West US region.</span></span>
<span data-ttu-id="ef295-112">Magazyn używa domyślnego typu magazynu nadmiarowego.</span><span class="sxs-lookup"><span data-stu-id="ef295-112">The vault uses the default GeoRedundant storage type.</span></span>

### <span data-ttu-id="ef295-113">Przykład 2: Tworzenie magazynu kopii zapasowych używającego lokalnie nadmiarowego miejsca do magazynowania</span><span class="sxs-lookup"><span data-stu-id="ef295-113">Example 2: Create a backup vault that uses locally redundant storage</span></span>
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup02" -Name "Vault03" -Region "westus" -Storage LocallyRedundant
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup02/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup02
Region            : westus
Storage           : LocallyRedundant
```

<span data-ttu-id="ef295-114">To polecenie tworzy magazyn kopii zapasowych Azure o nazwie Vault03.</span><span class="sxs-lookup"><span data-stu-id="ef295-114">This command creates an Azure Backup vault named Vault03.</span></span>
<span data-ttu-id="ef295-115">Magazyn znajduje się w grupie zasobów o nazwie ResourceGroup02 w zachodnim regionie Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="ef295-115">The vault is in the resource group named ResourceGroup02 in the West US region.</span></span>
<span data-ttu-id="ef295-116">Magazyn używa typu magazynu LocallyRedundant.</span><span class="sxs-lookup"><span data-stu-id="ef295-116">The vault uses the LocallyRedundant storage type.</span></span>

## <span data-ttu-id="ef295-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ef295-117">PARAMETERS</span></span>

### <span data-ttu-id="ef295-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef295-118">-DefaultProfile</span></span>
<span data-ttu-id="ef295-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ef295-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef295-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ef295-120">-Name</span></span>
<span data-ttu-id="ef295-121">Określa nazwę magazynu kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ef295-121">Specifies a name for the Azure Backup vault.</span></span>
<span data-ttu-id="ef295-122">Nazwa musi być unikatowa w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="ef295-122">The name must be unique in a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef295-123">-Region</span><span class="sxs-lookup"><span data-stu-id="ef295-123">-Region</span></span>
<span data-ttu-id="ef295-124">Określa obszar platformy Azure, w którym istnieje magazyn kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="ef295-124">Specifies an Azure region in which the backup vault exists.</span></span>
<span data-ttu-id="ef295-125">W przypadku scenariuszy hybrydowych kopii zapasowych zalecamy utworzenie magazynu w regionie blisko lokalnego serwera w celu skrócenia czasu oczekiwania.</span><span class="sxs-lookup"><span data-stu-id="ef295-125">For hybrid backup scenarios, we recommend that you create a vault in a region close to the on-premise server to reduce latency.</span></span>
<span data-ttu-id="ef295-126">Aby utworzyć kopię zapasową infrastruktury platformy Azure jako maszyn wirtualnych usługi (IaaS), magazyn staje się punktem odnajdowania lokalnych maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="ef295-126">For backup of Azure infrastructure as a service (IaaS) virtual machines, the vault becomes the point of discovery for local virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef295-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef295-127">-ResourceGroupName</span></span>
<span data-ttu-id="ef295-128">Określa nazwę istniejącej grupy zasobów platformy Azure, w której to polecenie cmdlet tworzy magazyn kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="ef295-128">Specifies the name of an existing Azure resource group in which this cmdlet creates a Backup vault.</span></span>
<span data-ttu-id="ef295-129">Aby utworzyć grupę zasobów, użyj polecenia cmdlet New-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ef295-129">To create a resource group, use the New-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="ef295-130">Grupa zasobów i magazyn kopii zapasowych Azure nie muszą znajdować się w tym samym regionie.</span><span class="sxs-lookup"><span data-stu-id="ef295-130">The resource group and the Azure Backup vault do not have to be in the same region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef295-131">-Storage</span><span class="sxs-lookup"><span data-stu-id="ef295-131">-Storage</span></span>
<span data-ttu-id="ef295-132">Określa typ magazynu dla danych kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="ef295-132">Specifies the storage type for the backup data.</span></span>
<span data-ttu-id="ef295-133">Dopuszczalne wartości tego parametru to: LocallyRedundant i geo.</span><span class="sxs-lookup"><span data-stu-id="ef295-133">The acceptable values for this parameter are: LocallyRedundant and GeoRedundant.</span></span>
<span data-ttu-id="ef295-134">Wartość domyślna jest zbyt nadmiarowa.</span><span class="sxs-lookup"><span data-stu-id="ef295-134">The default value is GeoRedundant.</span></span>

```yaml
Type: AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases: 
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef295-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef295-135">CommonParameters</span></span>
<span data-ttu-id="ef295-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef295-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef295-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef295-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef295-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef295-138">INPUTS</span></span>

### <span data-ttu-id="ef295-139">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ef295-139">None</span></span>

## <span data-ttu-id="ef295-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ef295-140">OUTPUTS</span></span>

### <span data-ttu-id="ef295-141">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="ef295-141">AzureRmBackupVault</span></span>

## <span data-ttu-id="ef295-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ef295-142">NOTES</span></span>
* <span data-ttu-id="ef295-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ef295-143">None</span></span>

## <span data-ttu-id="ef295-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef295-144">RELATED LINKS</span></span>

[<span data-ttu-id="ef295-145">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="ef295-145">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="ef295-146">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="ef295-146">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)

[<span data-ttu-id="ef295-147">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="ef295-147">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


