---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: F395E192-80FA-421D-A389-8C5C0C2267E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/sync-azmediaservicestoragekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
ms.openlocfilehash: 9ac16dec6403eb17f5c0bc352b7419aeb9854fec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194130"
---
# <span data-ttu-id="2190a-101">Sync-AzMediaServiceStorageKey</span><span class="sxs-lookup"><span data-stu-id="2190a-101">Sync-AzMediaServiceStorageKey</span></span>

## <span data-ttu-id="2190a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2190a-102">SYNOPSIS</span></span>
<span data-ttu-id="2190a-103">Synchronizuje klucze konta magazynu dla konta magazynu skojarzonego z usługą multimediów.</span><span class="sxs-lookup"><span data-stu-id="2190a-103">Synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="2190a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2190a-104">SYNTAX</span></span>

```
Sync-AzMediaServiceStorageKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-StorageAccountId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2190a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2190a-105">DESCRIPTION</span></span>
<span data-ttu-id="2190a-106">Polecenie **cmdlet Sync-AzMediaServiceStorageKey** synchronizuje klucze konta magazynu dla konta magazynu skojarzonego z usługą multimedialną.</span><span class="sxs-lookup"><span data-stu-id="2190a-106">The **Sync-AzMediaServiceStorageKey** cmdlet synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="2190a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2190a-107">EXAMPLES</span></span>

### <span data-ttu-id="2190a-108">Przykład 1. Synchronizowanie kluczy konta magazynu dla konta magazynu skojarzonego z usługą multimediów</span><span class="sxs-lookup"><span data-stu-id="2190a-108">Example 1: Synchronize storage account keys for a storage account associated with the media service</span></span>
```
PS C:\>$StorageAccount = Get-AzStorageAccount -ResourceGroupName "ResourceGroup001" -Name "Storage135"
PS C:\> Sync-AzMediaServiceStorageKey -ResourceGroupName "ResourceGroup001" -AccoutName "MediasService001" -StorageAccoutId $StorageAccount.Id
```

<span data-ttu-id="2190a-109">Pierwsze polecenie używa polecenia cmdlet Get-AzStorageAccount w celu uzyskania konta magazynu o nazwie Storage135, które należy do grupy ResourceGroup001, i przechowuje wynik w zmiennej o nazwie $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="2190a-109">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named Storage135 that belongs to ResourceGroup001 and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="2190a-110">Drugie polecenie synchronizuje klucze konta magazynu dla usługi multimediów o  nazwie MediaService001 przy użyciu właściwości Identyfikator zawartej w zmiennej $StorageAccount magazynu.</span><span class="sxs-lookup"><span data-stu-id="2190a-110">The second command synchronizes the storage account keys for the media service named MediaService001 using the **Id** property contained in the $StorageAccount variable.</span></span>

## <span data-ttu-id="2190a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2190a-111">PARAMETERS</span></span>

### <span data-ttu-id="2190a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2190a-112">-AccountName</span></span>
<span data-ttu-id="2190a-113">Określa nazwę usługi multimediów, która będzie synchronizowana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2190a-113">Specifies the name of the media service that this cmdlet synchronizes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2190a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2190a-114">-DefaultProfile</span></span>
<span data-ttu-id="2190a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="2190a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2190a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2190a-116">-ResourceGroupName</span></span>
<span data-ttu-id="2190a-117">Określa nazwę grupy zasobów zawierającej usługę multimediów.</span><span class="sxs-lookup"><span data-stu-id="2190a-117">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="2190a-118">- StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2190a-118">-StorageAccountId</span></span>
<span data-ttu-id="2190a-119">Określa identyfikator konta magazynu skojarzonego z kontem usługi multimediów.</span><span class="sxs-lookup"><span data-stu-id="2190a-119">Specifies the storage account ID associated with the media service account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2190a-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2190a-120">-Confirm</span></span>
<span data-ttu-id="2190a-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2190a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2190a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2190a-122">-WhatIf</span></span>
<span data-ttu-id="2190a-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2190a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2190a-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2190a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2190a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2190a-125">CommonParameters</span></span>
<span data-ttu-id="2190a-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2190a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2190a-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2190a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2190a-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2190a-128">INPUTS</span></span>

### <span data-ttu-id="2190a-129">System.String</span><span class="sxs-lookup"><span data-stu-id="2190a-129">System.String</span></span>

## <span data-ttu-id="2190a-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2190a-130">OUTPUTS</span></span>

### <span data-ttu-id="2190a-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2190a-131">System.Boolean</span></span>

## <span data-ttu-id="2190a-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2190a-132">NOTES</span></span>

## <span data-ttu-id="2190a-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2190a-133">RELATED LINKS</span></span>
