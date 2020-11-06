---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 542e75ed0e6531f5778f9793b678b42f953c15d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525033"
---
# <span data-ttu-id="f516a-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="f516a-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="f516a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f516a-102">SYNOPSIS</span></span>
<span data-ttu-id="f516a-103">Tworzy obiekt mapowania dysku dla dysków maszyny wirtualnej platformy Azure, które mają być replikowane.</span><span class="sxs-lookup"><span data-stu-id="f516a-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f516a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f516a-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f516a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f516a-105">DESCRIPTION</span></span>
<span data-ttu-id="f516a-106">Tworzy obiekt mapowania dysku, który mapuje dysk maszyny wirtualnej platformy Azure na konto magazynu w pamięci podręcznej i docelowe konto magazynu (region odzyskiwania) do użycia w celu zreplikowania dysku.</span><span class="sxs-lookup"><span data-stu-id="f516a-106">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="f516a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f516a-107">EXAMPLES</span></span>

### <span data-ttu-id="f516a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f516a-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="f516a-109">Utwórz obiekt mapowania dysku na potrzeby replikowania dysków maszyny wirtualnej platformy Azure. Używane podczas operacji włączania funkcji Azure to Azure do platformy Azure i ochrony.</span><span class="sxs-lookup"><span data-stu-id="f516a-109">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="f516a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f516a-110">PARAMETERS</span></span>

### <span data-ttu-id="f516a-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f516a-111">-Confirm</span></span>
<span data-ttu-id="f516a-112">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f516a-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f516a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f516a-113">-DefaultProfile</span></span>
<span data-ttu-id="f516a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f516a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f516a-115">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f516a-115">-LogStorageAccountId</span></span>
<span data-ttu-id="f516a-116">Określa identyfikator konta dziennika lub pamięci podręcznej, który ma być wykorzystywany do przechowywania dzienników replikacji.</span><span class="sxs-lookup"><span data-stu-id="f516a-116">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f516a-117">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f516a-117">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="f516a-118">Określa identyfikator konta usługi Azure Storage, do którego mają być replikowane dane.</span><span class="sxs-lookup"><span data-stu-id="f516a-118">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f516a-119">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="f516a-119">-VhdUri</span></span>
<span data-ttu-id="f516a-120">Określ identyfikator URI wirtualnego dysku twardego, do którego odnosi się to mapowanie.</span><span class="sxs-lookup"><span data-stu-id="f516a-120">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f516a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f516a-121">-WhatIf</span></span>
<span data-ttu-id="f516a-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f516a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f516a-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f516a-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f516a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f516a-124">CommonParameters</span></span>
<span data-ttu-id="f516a-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f516a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f516a-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f516a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f516a-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f516a-127">INPUTS</span></span>

### <span data-ttu-id="f516a-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f516a-128">None</span></span>

## <span data-ttu-id="f516a-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f516a-129">OUTPUTS</span></span>

### <span data-ttu-id="f516a-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="f516a-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="f516a-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f516a-131">NOTES</span></span>

## <span data-ttu-id="f516a-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f516a-132">RELATED LINKS</span></span>
