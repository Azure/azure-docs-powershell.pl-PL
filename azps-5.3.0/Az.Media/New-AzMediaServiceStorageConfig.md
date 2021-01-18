---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/new-azmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
ms.openlocfilehash: d53edc73bb1813841403348919758f1c6c13eff4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504523"
---
# <span data-ttu-id="dede2-101">New-AzMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="dede2-101">New-AzMediaServiceStorageConfig</span></span>

## <span data-ttu-id="dede2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dede2-102">SYNOPSIS</span></span>
<span data-ttu-id="dede2-103">Utwórz konfigurację konta magazynu dla poleceń cmdlet usługi multimediów.</span><span class="sxs-lookup"><span data-stu-id="dede2-103">Create a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="dede2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dede2-104">SYNTAX</span></span>

```
New-AzMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dede2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dede2-105">DESCRIPTION</span></span>
<span data-ttu-id="dede2-106">Polecenie cmdlet **New-AzMediaServiceStorageConfig** umożliwia utworzenie konfiguracji konta magazynu dla poleceń cmdlet usługi multimediów.</span><span class="sxs-lookup"><span data-stu-id="dede2-106">The **New-AzMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="dede2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dede2-107">EXAMPLES</span></span>

### <span data-ttu-id="dede2-108">Przykład 1. Tworzenie konfiguracji konta magazynu dla poleceń cmdlet usługi multimediów</span><span class="sxs-lookup"><span data-stu-id="dede2-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="dede2-109">Pierwsze polecenie tworzy obiekt konta magazynu przy użyciu polecenia cmdlet **New-AzStorageAccount** .</span><span class="sxs-lookup"><span data-stu-id="dede2-109">The first command creates a storage account object by using **the New-AzStorageAccount** cmdlet.</span></span>
<span data-ttu-id="dede2-110">Polecenie nadaje nazwę temu kontu Storage1, a typ ma nazwę Standard_GRS i zapisuje wynik w zmiennej o nazwie $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="dede2-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="dede2-111">Drugie polecenie tworzy obiekt konfiguracji magazynu jako główne konto magazynu skojarzone z usługą multimediów, korzystając z informacji o IDENTYFIKATORze konta magazynu przechowywanych w zmiennej $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="dede2-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="dede2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dede2-112">PARAMETERS</span></span>

### <span data-ttu-id="dede2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dede2-113">-DefaultProfile</span></span>
<span data-ttu-id="dede2-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="dede2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dede2-115">-Isprimary</span><span class="sxs-lookup"><span data-stu-id="dede2-115">-IsPrimary</span></span>
<span data-ttu-id="dede2-116">Wskazuje, że polecenie cmdlet tworzy konto magazynu jako magazyn podstawowy dla usługi multimedialnej.</span><span class="sxs-lookup"><span data-stu-id="dede2-116">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

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

### <span data-ttu-id="dede2-117">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="dede2-117">-StorageAccountId</span></span>
<span data-ttu-id="dede2-118">Określa identyfikator konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="dede2-118">Specifies the ID of the storage account.</span></span>

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

### <span data-ttu-id="dede2-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dede2-119">-Confirm</span></span>
<span data-ttu-id="dede2-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dede2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dede2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dede2-121">-WhatIf</span></span>
<span data-ttu-id="dede2-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dede2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dede2-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dede2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dede2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dede2-124">CommonParameters</span></span>
<span data-ttu-id="dede2-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dede2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dede2-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dede2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dede2-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dede2-127">INPUTS</span></span>

### <span data-ttu-id="dede2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="dede2-128">System.String</span></span>

## <span data-ttu-id="dede2-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dede2-129">OUTPUTS</span></span>

### <span data-ttu-id="dede2-130">Microsoft. Azure. Commands. Media. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dede2-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="dede2-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dede2-131">NOTES</span></span>

## <span data-ttu-id="dede2-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dede2-132">RELATED LINKS</span></span>

[<span data-ttu-id="dede2-133">Sync-AzMediaServiceStorageKey</span><span class="sxs-lookup"><span data-stu-id="dede2-133">Sync-AzMediaServiceStorageKey</span></span>](./Sync-AzMediaServiceStorageKey.md)


