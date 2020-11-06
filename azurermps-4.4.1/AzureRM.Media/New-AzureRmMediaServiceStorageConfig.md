---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaServiceStorageConfig.md
ms.openlocfilehash: 236486af937a99812f4979ed4db089002fb9ad30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549975"
---
# <span data-ttu-id="343f7-101">New-AzureRmMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="343f7-101">New-AzureRmMediaServiceStorageConfig</span></span>

## <span data-ttu-id="343f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="343f7-102">SYNOPSIS</span></span>
<span data-ttu-id="343f7-103">Utwórz konfigurację konta magazynu dla poleceń cmdlet usługi multimediów.</span><span class="sxs-lookup"><span data-stu-id="343f7-103">Create a storage account configuration for the media service cmdlets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="343f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="343f7-104">SYNTAX</span></span>

```
New-AzureRmMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="343f7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="343f7-105">DESCRIPTION</span></span>
<span data-ttu-id="343f7-106">Polecenie cmdlet **New-AzureRmMediaServiceStorageConfig** umożliwia utworzenie konfiguracji konta magazynu dla poleceń cmdlet usługi multimediów.</span><span class="sxs-lookup"><span data-stu-id="343f7-106">The **New-AzureRmMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="343f7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="343f7-107">EXAMPLES</span></span>

### <span data-ttu-id="343f7-108">Przykład 1. Tworzenie konfiguracji konta magazynu dla poleceń cmdlet usługi multimediów</span><span class="sxs-lookup"><span data-stu-id="343f7-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="343f7-109">Pierwsze polecenie tworzy obiekt konta magazynu przy użyciu polecenia cmdlet **New-AzureRmStorageAccount** .</span><span class="sxs-lookup"><span data-stu-id="343f7-109">The first command creates a storage account object by using **the New-AzureRmStorageAccount** cmdlet.</span></span>
<span data-ttu-id="343f7-110">Polecenie nadaje nazwę temu kontu Storage1, a typ ma nazwę Standard_GRS i zapisuje wynik w zmiennej o nazwie $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="343f7-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>

<span data-ttu-id="343f7-111">Drugie polecenie tworzy obiekt konfiguracji magazynu jako główne konto magazynu skojarzone z usługą multimediów, korzystając z informacji o IDENTYFIKATORze konta magazynu przechowywanych w zmiennej $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="343f7-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="343f7-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="343f7-112">PARAMETERS</span></span>

### <span data-ttu-id="343f7-113">-Isprimary</span><span class="sxs-lookup"><span data-stu-id="343f7-113">-IsPrimary</span></span>
<span data-ttu-id="343f7-114">Wskazuje, że polecenie cmdlet tworzy konto magazynu jako magazyn podstawowy dla usługi multimedialnej.</span><span class="sxs-lookup"><span data-stu-id="343f7-114">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="343f7-115">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="343f7-115">-StorageAccountId</span></span>
<span data-ttu-id="343f7-116">Określa identyfikator konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="343f7-116">Specifies the ID of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="343f7-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="343f7-117">-Confirm</span></span>
<span data-ttu-id="343f7-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="343f7-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="343f7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="343f7-119">-WhatIf</span></span>
<span data-ttu-id="343f7-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="343f7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="343f7-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="343f7-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="343f7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="343f7-122">-DefaultProfile</span></span>
<span data-ttu-id="343f7-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="343f7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="343f7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="343f7-124">CommonParameters</span></span>
<span data-ttu-id="343f7-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="343f7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="343f7-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="343f7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="343f7-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="343f7-127">INPUTS</span></span>

## <span data-ttu-id="343f7-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="343f7-128">OUTPUTS</span></span>

### <span data-ttu-id="343f7-129">Microsoft. Azure. Commands. Media. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="343f7-129">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="343f7-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="343f7-130">NOTES</span></span>

## <span data-ttu-id="343f7-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="343f7-131">RELATED LINKS</span></span>

[<span data-ttu-id="343f7-132">Sync-AzureRmMediaServiceStorageKeys</span><span class="sxs-lookup"><span data-stu-id="343f7-132">Sync-AzureRmMediaServiceStorageKeys</span></span>](./Sync-AzureRmMediaServiceStorageKeys.md)


