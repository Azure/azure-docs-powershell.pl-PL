---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: F395E192-80FA-421D-A389-8C5C0C2267E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/sync-azurermmediaservicestoragekeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Sync-AzureRmMediaServiceStorageKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Sync-AzureRmMediaServiceStorageKeys.md
ms.openlocfilehash: 1f61718a6812977b86e32b12cd8ce8bdafbde207
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545639"
---
# <span data-ttu-id="c1037-101">Sync-AzureRmMediaServiceStorageKeys</span><span class="sxs-lookup"><span data-stu-id="c1037-101">Sync-AzureRmMediaServiceStorageKeys</span></span>

## <span data-ttu-id="c1037-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c1037-102">SYNOPSIS</span></span>
<span data-ttu-id="c1037-103">Synchronizuje klucze konta magazynu dla konta magazynu skojarzonego z usługą multimediów.</span><span class="sxs-lookup"><span data-stu-id="c1037-103">Synchronizes storage account keys for a storage account associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1037-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c1037-104">SYNTAX</span></span>

```
Sync-AzureRmMediaServiceStorageKeys [-ResourceGroupName] <String> [-AccountName] <String>
 [-StorageAccountId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1037-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c1037-105">DESCRIPTION</span></span>
<span data-ttu-id="c1037-106">Polecenie cmdlet **Sync-AzureRmMediaServiceStorageKeys** synchronizuje klucze konta magazynu dla konta magazynu skojarzonego z usługą multimediów.</span><span class="sxs-lookup"><span data-stu-id="c1037-106">The **Sync-AzureRmMediaServiceStorageKeys** cmdlet synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="c1037-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c1037-107">EXAMPLES</span></span>

### <span data-ttu-id="c1037-108">Przykład 1: synchronizowanie kluczy konta magazynu dla konta magazynu skojarzonego z usługą multimediów</span><span class="sxs-lookup"><span data-stu-id="c1037-108">Example 1: Synchronize storage account keys for a storage account associated with the media service</span></span>
```
PS C:\>$StorageAccount = Get-AzureRmStorageAccount -ResourceGroupName "ResourceGroup001" -Name "Storage135"
PS C:\> Sync-AzureRmMediaServiceStorageKeys -ResourceGroupName "ResourceGroup001" -AccoutName "MediasService001" -StorageAccoutId $StorageAccount.Id
```

<span data-ttu-id="c1037-109">W pierwszym poleceniu użyto polecenia cmdlet Get-AzureRmStorageAccount, aby uzyskać konto magazynu o nazwie Storage135 należącego do ResourceGroup001 i przechowywać wynik w zmiennej o nazwie $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="c1037-109">The first command uses the Get-AzureRmStorageAccount cmdlet to get the storage account named Storage135 that belongs to ResourceGroup001 and stores the result in the variable named $StorageAccount.</span></span>

<span data-ttu-id="c1037-110">Drugie polecenie synchronizuje klucze konta magazynu dla usługi multimedialnej o nazwie MediaService001 przy użyciu właściwości **ID** zawartej w zmiennej $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="c1037-110">The second command synchronizes the storage account keys for the media service named MediaService001 using the **Id** property contained in the $StorageAccount variable.</span></span>

## <span data-ttu-id="c1037-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c1037-111">PARAMETERS</span></span>

### <span data-ttu-id="c1037-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c1037-112">-AccountName</span></span>
<span data-ttu-id="c1037-113">Określa nazwę usługi multimedialnej, która jest synchronizowana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1037-113">Specifies the name of the media service that this cmdlet synchronizes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1037-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1037-114">-DefaultProfile</span></span>
<span data-ttu-id="c1037-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c1037-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1037-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1037-116">-ResourceGroupName</span></span>
<span data-ttu-id="c1037-117">Określa nazwę grupy zasobów zawierającej usługę Media.</span><span class="sxs-lookup"><span data-stu-id="c1037-117">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1037-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c1037-118">-StorageAccountId</span></span>
<span data-ttu-id="c1037-119">Określa identyfikator konta magazynu skojarzonego z kontem usługi multimedialnej.</span><span class="sxs-lookup"><span data-stu-id="c1037-119">Specifies the storage account ID associated with the media service account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1037-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c1037-120">-Confirm</span></span>
<span data-ttu-id="c1037-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1037-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1037-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1037-122">-WhatIf</span></span>
<span data-ttu-id="c1037-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1037-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1037-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c1037-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1037-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1037-125">CommonParameters</span></span>
<span data-ttu-id="c1037-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1037-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1037-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1037-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1037-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1037-128">INPUTS</span></span>

### <span data-ttu-id="c1037-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c1037-129">None</span></span>
<span data-ttu-id="c1037-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="c1037-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c1037-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c1037-131">OUTPUTS</span></span>

### <span data-ttu-id="c1037-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c1037-132">System.Boolean</span></span>

## <span data-ttu-id="c1037-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c1037-133">NOTES</span></span>

## <span data-ttu-id="c1037-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c1037-134">RELATED LINKS</span></span>

