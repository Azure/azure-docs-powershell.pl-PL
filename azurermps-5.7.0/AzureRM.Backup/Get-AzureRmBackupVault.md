---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 95FF3F7A-5CC6-4AA6-A393-5EBB5579D9A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
ms.openlocfilehash: 18383ffeb35b1ce6bb2651be041e07b6164e55da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718962"
---
# <span data-ttu-id="32912-101">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="32912-101">Get-AzureRmBackupVault</span></span>

## <span data-ttu-id="32912-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="32912-102">SYNOPSIS</span></span>
<span data-ttu-id="32912-103">Pobiera magazyny kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="32912-103">Gets Backup vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32912-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="32912-104">SYNTAX</span></span>

```
Get-AzureRmBackupVault [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32912-105">Opis</span><span class="sxs-lookup"><span data-stu-id="32912-105">DESCRIPTION</span></span>
<span data-ttu-id="32912-106">Polecenie cmdlet **Get-AzureRmBackupVault** pobiera magazyny kopii zapasowych Azure.</span><span class="sxs-lookup"><span data-stu-id="32912-106">The **Get-AzureRmBackupVault** cmdlet gets Azure Backup vaults.</span></span>
<span data-ttu-id="32912-107">To polecenie cmdlet zwraca obiekty **AzureRmBackupVault** , które mają być używane z innymi poleceniami cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32912-107">This cmdlet returns **AzureRmBackupVault** objects for use with other cmdlets.</span></span>

## <span data-ttu-id="32912-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="32912-108">EXAMPLES</span></span>

### <span data-ttu-id="32912-109">Przykład 1: wyświetlanie wszystkich magazynów kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="32912-109">Example 1: View all the Backup vaults</span></span>
```
PS C:\>Get-AzureRmBackupVault
```

<span data-ttu-id="32912-110">To polecenie pobiera wszystkie magazyny kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="32912-110">This command gets all the Azure Backup vaults.</span></span>

### <span data-ttu-id="32912-111">Przykład 2: wyświetlanie wszystkich magazynów utworzonych w STANach na zachód</span><span class="sxs-lookup"><span data-stu-id="32912-111">Example 2: View all vaults created in West US</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Region -eq "westus" }
```

<span data-ttu-id="32912-112">To polecenie pobiera wszystkie magazyny kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="32912-112">This command gets all the Backup vaults.</span></span>
<span data-ttu-id="32912-113">Polecenie przekazuje je do polecenia cmdlet Where-Object przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="32912-113">The command passes them to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="32912-114">Polecenie cmdlet filtruje wyniki na podstawie właściwości **region** .</span><span class="sxs-lookup"><span data-stu-id="32912-114">That cmdlet filters the results based on the **Region** property.</span></span>
<span data-ttu-id="32912-115">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Where-Object` .</span><span class="sxs-lookup"><span data-stu-id="32912-115">For more information, type `Get-Help Where-Object`.</span></span>

### <span data-ttu-id="32912-116">Przykład 3: uzyskiwanie określonego magazynu</span><span class="sxs-lookup"><span data-stu-id="32912-116">Example 3: Get a specific vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup011/providers/Microsoft.Backup
                    /BackupVault/Vault
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

<span data-ttu-id="32912-117">To polecenie pobiera magazyn o nazwie Vault03.</span><span class="sxs-lookup"><span data-stu-id="32912-117">This command gets the vault named Vault03.</span></span>

### <span data-ttu-id="32912-118">Przykład 4: zliczanie magazynów z lokalnie nadmiarowym magazynem</span><span class="sxs-lookup"><span data-stu-id="32912-118">Example 4: Count the number of vaults that have locally redundant storage</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Storage -match "LocallyRedundant" } | Measure-Object
Count    : 4
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property :
```

<span data-ttu-id="32912-119">To polecenie pobiera wszystkie magazyny kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="32912-119">This command gets all the Azure Backup vaults.</span></span>
<span data-ttu-id="32912-120">Polecenie przekazuje je do **obiektu WHERE-Object** , który filtruje wyniki na podstawie właściwości **magazynu** .</span><span class="sxs-lookup"><span data-stu-id="32912-120">The command passes them to **Where-Object** , which filters the results based on the **Storage** property.</span></span>
<span data-ttu-id="32912-121">Polecenie przekazuje te elementy, które mają wartość LocallyRedundant, do polecenia cmdlet Measure-Object, które zlicza wyniki.</span><span class="sxs-lookup"><span data-stu-id="32912-121">The command passes the ones that have a value of LocallyRedundant to the Measure-Object cmdlet, which counts the results.</span></span>
<span data-ttu-id="32912-122">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Measure-Object` .</span><span class="sxs-lookup"><span data-stu-id="32912-122">For more information, type `Get-Help Measure-Object`.</span></span>

## <span data-ttu-id="32912-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="32912-123">PARAMETERS</span></span>

### <span data-ttu-id="32912-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32912-124">-DefaultProfile</span></span>
<span data-ttu-id="32912-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="32912-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32912-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="32912-126">-Name</span></span>
<span data-ttu-id="32912-127">Określa nazwę magazynu kopii zapasowych, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32912-127">Specifies the name of the Backup vault that this cmdlet gets.</span></span>
<span data-ttu-id="32912-128">Jeśli więcej niż jeden magazyn kopii zapasowych ma taką samą nazwę, to polecenie cmdlet zwróci je wszystkie.</span><span class="sxs-lookup"><span data-stu-id="32912-128">If more than one Backup vault has the same name, this cmdlet returns them all.</span></span>
<span data-ttu-id="32912-129">Określ parametr *ResourceGroupName* , aby uzyskać unikatowy magazyn.</span><span class="sxs-lookup"><span data-stu-id="32912-129">Specify the *ResourceGroupName* parameter to get a unique vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32912-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32912-130">-ResourceGroupName</span></span>
<span data-ttu-id="32912-131">Określa nazwę grupy zasobów platformy Azure, w której to polecenie cmdlet pobiera magazyn kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="32912-131">Specifies the name of an Azure resource group in which this cmdlet gets a Backup vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32912-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32912-132">CommonParameters</span></span>
<span data-ttu-id="32912-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32912-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32912-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32912-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32912-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32912-135">INPUTS</span></span>

### <span data-ttu-id="32912-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="32912-136">None</span></span>
<span data-ttu-id="32912-137">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="32912-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="32912-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="32912-138">OUTPUTS</span></span>

### <span data-ttu-id="32912-139">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="32912-139">AzureRmBackupVault</span></span>

## <span data-ttu-id="32912-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="32912-140">NOTES</span></span>
* <span data-ttu-id="32912-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="32912-141">None</span></span>

## <span data-ttu-id="32912-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="32912-142">RELATED LINKS</span></span>

[<span data-ttu-id="32912-143">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="32912-143">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="32912-144">Nowe — AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="32912-144">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="32912-145">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="32912-145">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)

[<span data-ttu-id="32912-146">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="32912-146">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


