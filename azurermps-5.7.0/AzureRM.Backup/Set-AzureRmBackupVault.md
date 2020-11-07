---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: D57C32D1-EB4F-495E-A11B-3B4066E8C552
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
ms.openlocfilehash: f578fa3aab2cf89dcb8d3a753855ded57eaf35db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718049"
---
# <span data-ttu-id="7eb12-101">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="7eb12-101">Set-AzureRmBackupVault</span></span>

## <span data-ttu-id="7eb12-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7eb12-102">SYNOPSIS</span></span>
<span data-ttu-id="7eb12-103">Zmienia typ magazynowania magazynu kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="7eb12-103">Changes the storage type of a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7eb12-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7eb12-104">SYNTAX</span></span>

```
Set-AzureRmBackupVault [[-Storage] <AzureBackupVaultStorageType>] [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7eb12-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7eb12-105">DESCRIPTION</span></span>
<span data-ttu-id="7eb12-106">Polecenie cmdlet **Set-AzureRmBackupVault** zmienia typ magazynu magazynu kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7eb12-106">The **Set-AzureRmBackupVault** cmdlet changes the storage type of an Azure Backup vault.</span></span>
<span data-ttu-id="7eb12-107">Nie można modyfikować innych właściwości magazynu.</span><span class="sxs-lookup"><span data-stu-id="7eb12-107">You cannot modify other properties of a vault.</span></span>

## <span data-ttu-id="7eb12-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7eb12-108">EXAMPLES</span></span>

### <span data-ttu-id="7eb12-109">Przykład 1. zmiana miejsca do magazynowania w istniejącym magazynie</span><span class="sxs-lookup"><span data-stu-id="7eb12-109">Example 1: Change the storage for an existing vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Set-AzureRmBackupVault -Storage LocallyRedundant
```

<span data-ttu-id="7eb12-110">To polecenie pobiera magazyn kopii zapasowych Azure o nazwie Vault03 przy użyciu polecenia cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="7eb12-110">This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="7eb12-111">Polecenie przekazuje ten magazyn do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="7eb12-111">The command passes that vault to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7eb12-112">Bieżące polecenie cmdlet zmienia typ magazynu na LocallyRedundant.</span><span class="sxs-lookup"><span data-stu-id="7eb12-112">The current cmdlet changes the storage type to LocallyRedundant.</span></span>

## <span data-ttu-id="7eb12-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7eb12-113">PARAMETERS</span></span>

### <span data-ttu-id="7eb12-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eb12-114">-DefaultProfile</span></span>
<span data-ttu-id="7eb12-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7eb12-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7eb12-116">-Storage</span><span class="sxs-lookup"><span data-stu-id="7eb12-116">-Storage</span></span>
<span data-ttu-id="7eb12-117">Określa typ magazynu dla danych kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="7eb12-117">Specifies the storage type for the backup data.</span></span>
<span data-ttu-id="7eb12-118">Dopuszczalne wartości tego parametru to: LocallyRedundant i geo.</span><span class="sxs-lookup"><span data-stu-id="7eb12-118">The acceptable values for this parameter are: LocallyRedundant and GeoRedundant.</span></span>

```yaml
Type: AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases: 
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eb12-119">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="7eb12-119">-Vault</span></span>
<span data-ttu-id="7eb12-120">Określa magazyn kopii zapasowych, który jest modyfikowany przez ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="7eb12-120">Specifies a Backup vault that this cmdlet modifies.</span></span>
<span data-ttu-id="7eb12-121">Aby uzyskać obiekt **AzureRmBackupVault** , użyj polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="7eb12-121">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="7eb12-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eb12-122">CommonParameters</span></span>
<span data-ttu-id="7eb12-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eb12-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eb12-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eb12-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eb12-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7eb12-125">INPUTS</span></span>

### <span data-ttu-id="7eb12-126">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="7eb12-126">AzureRmBackupVault</span></span>

## <span data-ttu-id="7eb12-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7eb12-127">OUTPUTS</span></span>

### <span data-ttu-id="7eb12-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7eb12-128">None</span></span>

## <span data-ttu-id="7eb12-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7eb12-129">NOTES</span></span>
* <span data-ttu-id="7eb12-130">Po zarejestrowaniu pierwszego serwera lub maszyny wirtualnej dla magazynu typ magazynu jest zablokowany.</span><span class="sxs-lookup"><span data-stu-id="7eb12-130">When you register the first server or virtual machine for a vault, the storage type is locked.</span></span> <span data-ttu-id="7eb12-131">Następnie nie można zmienić typu magazynu.</span><span class="sxs-lookup"><span data-stu-id="7eb12-131">Subsequently, you cannot change the storage type.</span></span>

## <span data-ttu-id="7eb12-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7eb12-132">RELATED LINKS</span></span>

[<span data-ttu-id="7eb12-133">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="7eb12-133">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="7eb12-134">Nowe — AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="7eb12-134">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="7eb12-135">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="7eb12-135">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)


