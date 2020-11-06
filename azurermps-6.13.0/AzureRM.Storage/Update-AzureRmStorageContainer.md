---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/update-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageContainer.md
ms.openlocfilehash: 9e4f62ef28d4cbcb22ddb563e558ad5d48733360
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547287"
---
# <span data-ttu-id="9b76f-101">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9b76f-101">Update-AzureRmStorageContainer</span></span>

## <span data-ttu-id="9b76f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9b76f-102">SYNOPSIS</span></span>
<span data-ttu-id="9b76f-103">Modyfikuje kontener obiektu BLOB przechowywania</span><span class="sxs-lookup"><span data-stu-id="9b76f-103">Modifies a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b76f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9b76f-104">SYNTAX</span></span>

### <span data-ttu-id="9b76f-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="9b76f-105">AccountName (Default)</span></span>
```
Update-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name] <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b76f-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="9b76f-106">AccountObject</span></span>
```
Update-AzureRmStorageContainer [-Name] <String> -StorageAccount <PSStorageAccount>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b76f-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="9b76f-107">ContainerObject</span></span>
```
Update-AzureRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b76f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9b76f-108">DESCRIPTION</span></span>
<span data-ttu-id="9b76f-109">Polecenie cmdlet **Update-AzureRmStorageContainer** modyfikuje kontener obiektu BLOB przechowywania</span><span class="sxs-lookup"><span data-stu-id="9b76f-109">The **Update-AzureRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="9b76f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9b76f-110">EXAMPLES</span></span>

### <span data-ttu-id="9b76f-111">Przykład 1: modyfikuje metadane kontenera obiektu blob magazynu i dostęp publiczny przy użyciu nazwy konta magazynu i nazwy kontenera</span><span class="sxs-lookup"><span data-stu-id="9b76f-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"} 
```

<span data-ttu-id="9b76f-112">To polecenie modyfikuje metadane kontenera obiektów blob magazynu i dostęp publiczny przy użyciu nazwy konta magazynu i nazwy kontenera.</span><span class="sxs-lookup"><span data-stu-id="9b76f-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="9b76f-113">Przykład 2: wyłączanie dostępu publicznego w kontenerze obiektu blob magazynu przy użyciu obiektu konta magazynu i nazwy kontenera</span><span class="sxs-lookup"><span data-stu-id="9b76f-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="9b76f-114">To polecenie wyłącza dostęp publiczny w kontenerze obiektu blob magazynu przy użyciu obiektu konta magazynu i nazwy kontenera.</span><span class="sxs-lookup"><span data-stu-id="9b76f-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="9b76f-115">Przykład 3: Ustawianie dostępu publicznego jako obiektu BLOB dla wszystkich kontenerów obiektów blob magazynu na koncie magazynu z potokiem</span><span class="sxs-lookup"><span data-stu-id="9b76f-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzureRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="9b76f-116">To polecenie ustawia dostęp publiczny jako obiekt BLOB dla wszystkich kontenerów blob magazynu na koncie magazynu z potokiem.</span><span class="sxs-lookup"><span data-stu-id="9b76f-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="9b76f-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9b76f-117">PARAMETERS</span></span>

### <span data-ttu-id="9b76f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b76f-118">-DefaultProfile</span></span>
<span data-ttu-id="9b76f-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b76f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b76f-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9b76f-120">-InputObject</span></span>
<span data-ttu-id="9b76f-121">Obiekt kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="9b76f-121">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b76f-122">-Metadata</span><span class="sxs-lookup"><span data-stu-id="9b76f-122">-Metadata</span></span>
<span data-ttu-id="9b76f-123">Metadane kontenera</span><span class="sxs-lookup"><span data-stu-id="9b76f-123">Container Metadata</span></span>

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

### <span data-ttu-id="9b76f-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9b76f-124">-Name</span></span>
<span data-ttu-id="9b76f-125">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="9b76f-125">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b76f-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="9b76f-126">-PublicAccess</span></span>
<span data-ttu-id="9b76f-127">Kontener PublicAccess</span><span class="sxs-lookup"><span data-stu-id="9b76f-127">Container PublicAccess</span></span>

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

### <span data-ttu-id="9b76f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b76f-128">-ResourceGroupName</span></span>
<span data-ttu-id="9b76f-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9b76f-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="9b76f-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="9b76f-130">-StorageAccount</span></span>
<span data-ttu-id="9b76f-131">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="9b76f-131">Storage account object</span></span>

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

### <span data-ttu-id="9b76f-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9b76f-132">-StorageAccountName</span></span>
<span data-ttu-id="9b76f-133">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="9b76f-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="9b76f-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9b76f-134">-Confirm</span></span>
<span data-ttu-id="9b76f-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b76f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b76f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b76f-136">-WhatIf</span></span>
<span data-ttu-id="9b76f-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b76f-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b76f-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9b76f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b76f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b76f-139">CommonParameters</span></span>
<span data-ttu-id="9b76f-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b76f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b76f-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b76f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b76f-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b76f-142">INPUTS</span></span>

### <span data-ttu-id="9b76f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="9b76f-143">System.String</span></span>

## <span data-ttu-id="9b76f-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9b76f-144">OUTPUTS</span></span>

### <span data-ttu-id="9b76f-145">Microsoft. Azure. Commands. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="9b76f-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="9b76f-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9b76f-146">NOTES</span></span>

## <span data-ttu-id="9b76f-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b76f-147">RELATED LINKS</span></span>

