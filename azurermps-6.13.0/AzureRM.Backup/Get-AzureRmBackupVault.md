---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 95FF3F7A-5CC6-4AA6-A393-5EBB5579D9A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
ms.openlocfilehash: c11170e6bee80b9eaa19135ad604d8bf70e1baab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717945"
---
# <span data-ttu-id="d7ce7-101">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="d7ce7-101">Get-AzureRmBackupVault</span></span>

## <span data-ttu-id="d7ce7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7ce7-102">SYNOPSIS</span></span>
<span data-ttu-id="d7ce7-103">Pobiera magazyny kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-103">Gets Backup vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7ce7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7ce7-104">SYNTAX</span></span>

```
Get-AzureRmBackupVault [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7ce7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d7ce7-105">DESCRIPTION</span></span>
<span data-ttu-id="d7ce7-106">Polecenie cmdlet **Get-AzureRmBackupVault** pobiera magazyny kopii zapasowych Azure.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-106">The **Get-AzureRmBackupVault** cmdlet gets Azure Backup vaults.</span></span>
<span data-ttu-id="d7ce7-107">To polecenie cmdlet zwraca obiekty **AzureRmBackupVault** , które mają być używane z innymi poleceniami cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-107">This cmdlet returns **AzureRmBackupVault** objects for use with other cmdlets.</span></span>

## <span data-ttu-id="d7ce7-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7ce7-108">EXAMPLES</span></span>

### <span data-ttu-id="d7ce7-109">Przykład 1: wyświetlanie wszystkich magazynów kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="d7ce7-109">Example 1: View all the Backup vaults</span></span>
```
PS C:\>Get-AzureRmBackupVault
```

<span data-ttu-id="d7ce7-110">To polecenie pobiera wszystkie magazyny kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-110">This command gets all the Azure Backup vaults.</span></span>

### <span data-ttu-id="d7ce7-111">Przykład 2: wyświetlanie wszystkich magazynów utworzonych w STANach na zachód</span><span class="sxs-lookup"><span data-stu-id="d7ce7-111">Example 2: View all vaults created in West US</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Region -eq "westus" }
```

<span data-ttu-id="d7ce7-112">To polecenie pobiera wszystkie magazyny kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-112">This command gets all the Backup vaults.</span></span>
<span data-ttu-id="d7ce7-113">Polecenie przekazuje je do polecenia cmdlet Where-Object przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-113">The command passes them to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d7ce7-114">Polecenie cmdlet filtruje wyniki na podstawie właściwości **region** .</span><span class="sxs-lookup"><span data-stu-id="d7ce7-114">That cmdlet filters the results based on the **Region** property.</span></span>
<span data-ttu-id="d7ce7-115">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Where-Object` .</span><span class="sxs-lookup"><span data-stu-id="d7ce7-115">For more information, type `Get-Help Where-Object`.</span></span>

### <span data-ttu-id="d7ce7-116">Przykład 3: uzyskiwanie określonego magazynu</span><span class="sxs-lookup"><span data-stu-id="d7ce7-116">Example 3: Get a specific vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup011/providers/Microsoft.Backup
                    /BackupVault/Vault
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

<span data-ttu-id="d7ce7-117">To polecenie pobiera magazyn o nazwie Vault03.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-117">This command gets the vault named Vault03.</span></span>

### <span data-ttu-id="d7ce7-118">Przykład 4: zliczanie magazynów z lokalnie nadmiarowym magazynem</span><span class="sxs-lookup"><span data-stu-id="d7ce7-118">Example 4: Count the number of vaults that have locally redundant storage</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Storage -match "LocallyRedundant" } | Measure-Object
Count    : 4
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property :
```

<span data-ttu-id="d7ce7-119">To polecenie pobiera wszystkie magazyny kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-119">This command gets all the Azure Backup vaults.</span></span>
<span data-ttu-id="d7ce7-120">Polecenie przekazuje je do **obiektu WHERE-Object** , który filtruje wyniki na podstawie właściwości **magazynu** .</span><span class="sxs-lookup"><span data-stu-id="d7ce7-120">The command passes them to **Where-Object** , which filters the results based on the **Storage** property.</span></span>
<span data-ttu-id="d7ce7-121">Polecenie przekazuje te elementy, które mają wartość LocallyRedundant, do polecenia cmdlet Measure-Object, które zlicza wyniki.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-121">The command passes the ones that have a value of LocallyRedundant to the Measure-Object cmdlet, which counts the results.</span></span>
<span data-ttu-id="d7ce7-122">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Measure-Object` .</span><span class="sxs-lookup"><span data-stu-id="d7ce7-122">For more information, type `Get-Help Measure-Object`.</span></span>

## <span data-ttu-id="d7ce7-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7ce7-123">PARAMETERS</span></span>

### <span data-ttu-id="d7ce7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7ce7-124">-DefaultProfile</span></span>
<span data-ttu-id="d7ce7-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d7ce7-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7ce7-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d7ce7-126">-Name</span></span>
<span data-ttu-id="d7ce7-127">Określa nazwę magazynu kopii zapasowych, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-127">Specifies the name of the Backup vault that this cmdlet gets.</span></span>
<span data-ttu-id="d7ce7-128">Jeśli więcej niż jeden magazyn kopii zapasowych ma taką samą nazwę, to polecenie cmdlet zwróci je wszystkie.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-128">If more than one Backup vault has the same name, this cmdlet returns them all.</span></span>
<span data-ttu-id="d7ce7-129">Określ parametr *ResourceGroupName* , aby uzyskać unikatowy magazyn.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-129">Specify the *ResourceGroupName* parameter to get a unique vault.</span></span>

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

### <span data-ttu-id="d7ce7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7ce7-130">-ResourceGroupName</span></span>
<span data-ttu-id="d7ce7-131">Określa nazwę grupy zasobów platformy Azure, w której to polecenie cmdlet pobiera magazyn kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-131">Specifies the name of an Azure resource group in which this cmdlet gets a Backup vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ce7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7ce7-132">CommonParameters</span></span>
<span data-ttu-id="d7ce7-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7ce7-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7ce7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7ce7-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7ce7-135">INPUTS</span></span>

### <span data-ttu-id="d7ce7-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d7ce7-136">None</span></span>

## <span data-ttu-id="d7ce7-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7ce7-137">OUTPUTS</span></span>

### <span data-ttu-id="d7ce7-138">Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="d7ce7-138">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>

## <span data-ttu-id="d7ce7-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7ce7-139">NOTES</span></span>

## <span data-ttu-id="d7ce7-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7ce7-140">RELATED LINKS</span></span>

[<span data-ttu-id="d7ce7-141">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="d7ce7-141">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="d7ce7-142">Nowe — AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="d7ce7-142">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="d7ce7-143">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="d7ce7-143">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)

[<span data-ttu-id="d7ce7-144">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="d7ce7-144">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


