---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageContainer.md
ms.openlocfilehash: 8e136188a2857b53b566d30c439e222caea16abb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525962"
---
# <span data-ttu-id="04370-101">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="04370-101">New-AzureRmStorageContainer</span></span>

## <span data-ttu-id="04370-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="04370-102">SYNOPSIS</span></span>
<span data-ttu-id="04370-103">Tworzy kontener obiektu blob magazynu</span><span class="sxs-lookup"><span data-stu-id="04370-103">Creates a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04370-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="04370-104">SYNTAX</span></span>

### <span data-ttu-id="04370-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="04370-105">AccountName (Default)</span></span>
```
New-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name] <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04370-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="04370-106">AccountObject</span></span>
```
New-AzureRmStorageContainer -StorageAccount <PSStorageAccount> [-Name] <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04370-107">Opis</span><span class="sxs-lookup"><span data-stu-id="04370-107">DESCRIPTION</span></span>
<span data-ttu-id="04370-108">Polecenie cmdlet **New-AzureRmStorageContainer** tworzy kontener obiektu BLOB magazynowania</span><span class="sxs-lookup"><span data-stu-id="04370-108">The **New-AzureRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="04370-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="04370-109">EXAMPLES</span></span>

### <span data-ttu-id="04370-110">Przykład 1: Tworzenie kontenera obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera z metadanymi</span><span class="sxs-lookup"><span data-stu-id="04370-110">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"} 
```

<span data-ttu-id="04370-111">To polecenie tworzy kontener obiektu BLOB przechowywania z nazwą konta magazynu i nazwą kontenera z metadanymi.</span><span class="sxs-lookup"><span data-stu-id="04370-111">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="04370-112">Przykład 2: Tworzenie kontenera obiektów BLOB magazynowania z obiektem konta magazynu i nazwą kontenera z dostępem publicznym jako obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="04370-112">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="04370-113">To polecenie tworzy kontener obiektu BLOB magazynowania z obiektem konta magazynu i nazwą kontenera z dostępem publicznym jako obiekt BLOB.</span><span class="sxs-lookup"><span data-stu-id="04370-113">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

## <span data-ttu-id="04370-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="04370-114">PARAMETERS</span></span>

### <span data-ttu-id="04370-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04370-115">-DefaultProfile</span></span>
<span data-ttu-id="04370-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="04370-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04370-117">-Metadata</span><span class="sxs-lookup"><span data-stu-id="04370-117">-Metadata</span></span>
<span data-ttu-id="04370-118">Metadane kontenera</span><span class="sxs-lookup"><span data-stu-id="04370-118">Container Metadata</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04370-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="04370-119">-Name</span></span>
<span data-ttu-id="04370-120">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="04370-120">Container Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04370-121">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="04370-121">-PublicAccess</span></span>
<span data-ttu-id="04370-122">Kontener PublicAccess</span><span class="sxs-lookup"><span data-stu-id="04370-122">Container PublicAccess</span></span>

```yaml
Type: PSPublicAccess
Parameter Sets: (All)
Aliases: 
Accepted values: Container, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04370-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04370-123">-ResourceGroupName</span></span>
<span data-ttu-id="04370-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="04370-124">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04370-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="04370-125">-StorageAccount</span></span>
<span data-ttu-id="04370-126">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="04370-126">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04370-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="04370-127">-StorageAccountName</span></span>
<span data-ttu-id="04370-128">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="04370-128">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04370-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="04370-129">-Confirm</span></span>
<span data-ttu-id="04370-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04370-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04370-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04370-131">-WhatIf</span></span>
<span data-ttu-id="04370-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04370-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04370-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="04370-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04370-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04370-134">CommonParameters</span></span>
<span data-ttu-id="04370-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04370-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04370-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04370-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04370-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04370-137">INPUTS</span></span>

### <span data-ttu-id="04370-138">System. String</span><span class="sxs-lookup"><span data-stu-id="04370-138">System.String</span></span>

## <span data-ttu-id="04370-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="04370-139">OUTPUTS</span></span>

### <span data-ttu-id="04370-140">Microsoft. Azure. Commands. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="04370-140">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="04370-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="04370-141">NOTES</span></span>

## <span data-ttu-id="04370-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04370-142">RELATED LINKS</span></span>

