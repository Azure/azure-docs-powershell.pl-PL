---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/new-azmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
ms.openlocfilehash: ec411d7e1afd71849ec2d490ee70eeb0283303ca
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413816"
---
# <span data-ttu-id="595da-101">New-AzMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="595da-101">New-AzMediaServiceStorageConfig</span></span>

## <span data-ttu-id="595da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="595da-102">SYNOPSIS</span></span>
<span data-ttu-id="595da-103">Utwórz konfigurację konta magazynu dla cmdlet usługi multimediów.</span><span class="sxs-lookup"><span data-stu-id="595da-103">Create a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="595da-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="595da-104">SYNTAX</span></span>

```
New-AzMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="595da-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="595da-105">DESCRIPTION</span></span>
<span data-ttu-id="595da-106">Polecenie **cmdlet New-AzMediaServiceStorageConfig** tworzy konfigurację konta magazynu dla cmdlet usługi multimediów.</span><span class="sxs-lookup"><span data-stu-id="595da-106">The **New-AzMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="595da-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="595da-107">EXAMPLES</span></span>

### <span data-ttu-id="595da-108">Przykład 1. Tworzenie konfiguracji konta magazynu dla cmdlet usługi multimediów</span><span class="sxs-lookup"><span data-stu-id="595da-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="595da-109">Pierwsze polecenie tworzy obiekt konta magazynu przy użyciu polecenia cmdlet **New-AzStorageAccount.**</span><span class="sxs-lookup"><span data-stu-id="595da-109">The first command creates a storage account object by using **the New-AzStorageAccount** cmdlet.</span></span>
<span data-ttu-id="595da-110">To konto magazynu ma nazwę Magazyn1, a typ nosi nazwę Standard_GRS i zapisuje wynik w zmiennej o nazwie $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="595da-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="595da-111">Drugie polecenie tworzy obiekt konfiguracji magazynu jako podstawowe konto magazynu skojarzone z usługą multimediów przy użyciu informacji o identyfikatorze konta magazynu przechowywanych w $StorageAccount magazynu.</span><span class="sxs-lookup"><span data-stu-id="595da-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="595da-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="595da-112">PARAMETERS</span></span>

### <span data-ttu-id="595da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="595da-113">-DefaultProfile</span></span>
<span data-ttu-id="595da-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="595da-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="595da-115">-IsPrimary</span><span class="sxs-lookup"><span data-stu-id="595da-115">-IsPrimary</span></span>
<span data-ttu-id="595da-116">Wskazuje, że polecenie cmdlet tworzy konto magazynu jako podstawowy magazyn dla usługi multimediów.</span><span class="sxs-lookup"><span data-stu-id="595da-116">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

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

### <span data-ttu-id="595da-117">- StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="595da-117">-StorageAccountId</span></span>
<span data-ttu-id="595da-118">Określa identyfikator konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="595da-118">Specifies the ID of the storage account.</span></span>

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

### <span data-ttu-id="595da-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="595da-119">-Confirm</span></span>
<span data-ttu-id="595da-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="595da-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="595da-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="595da-121">-WhatIf</span></span>
<span data-ttu-id="595da-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="595da-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="595da-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="595da-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="595da-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="595da-124">CommonParameters</span></span>
<span data-ttu-id="595da-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="595da-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="595da-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="595da-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="595da-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="595da-127">INPUTS</span></span>

### <span data-ttu-id="595da-128">System.String</span><span class="sxs-lookup"><span data-stu-id="595da-128">System.String</span></span>

## <span data-ttu-id="595da-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="595da-129">OUTPUTS</span></span>

### <span data-ttu-id="595da-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="595da-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="595da-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="595da-131">NOTES</span></span>

## <span data-ttu-id="595da-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="595da-132">RELATED LINKS</span></span>



