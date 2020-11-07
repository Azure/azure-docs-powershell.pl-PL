---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainer.md
ms.openlocfilehash: 089451a0a0aae399a18296fbf4982724b35d432e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719057"
---
# <span data-ttu-id="b1fc6-101">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b1fc6-101">Remove-AzureRmStorageContainer</span></span>

## <span data-ttu-id="b1fc6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b1fc6-102">SYNOPSIS</span></span>
<span data-ttu-id="b1fc6-103">Usuwa kontener obiektu blob magazynu</span><span class="sxs-lookup"><span data-stu-id="b1fc6-103">Removes a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1fc6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b1fc6-104">SYNTAX</span></span>

### <span data-ttu-id="b1fc6-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="b1fc6-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1fc6-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="b1fc6-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1fc6-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="b1fc6-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1fc6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b1fc6-108">DESCRIPTION</span></span>
<span data-ttu-id="b1fc6-109">Polecenie cmdlet **Remove-AzureRmStorageContainer** usuwa kontener obiektu BLOB magazynowania</span><span class="sxs-lookup"><span data-stu-id="b1fc6-109">The **Remove-AzureRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="b1fc6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b1fc6-110">EXAMPLES</span></span>

### <span data-ttu-id="b1fc6-111">Przykład 1. Usuń kontener obiektu blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="b1fc6-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="b1fc6-112">To polecenie usuwa kontener obiektu blob magazynu z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="b1fc6-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="b1fc6-113">Przykład 2: usuwanie kontenera obiektu blob magazynu z obiektem konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="b1fc6-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="b1fc6-114">To polecenie usuwa kontener obiektu blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="b1fc6-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="b1fc6-115">Przykład 3: Usuwanie wszystkich kontenerów obiektów blob magazynu na koncie magazynu z potokiem</span><span class="sxs-lookup"><span data-stu-id="b1fc6-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzureRmStorageContainer -Force
```

<span data-ttu-id="b1fc6-116">To polecenie usuwa wszystkie kontenery obiektów blob magazynu z konta magazynu z potokiem.</span><span class="sxs-lookup"><span data-stu-id="b1fc6-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="b1fc6-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b1fc6-117">PARAMETERS</span></span>

### <span data-ttu-id="b1fc6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1fc6-118">-DefaultProfile</span></span>
<span data-ttu-id="b1fc6-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b1fc6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1fc6-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b1fc6-120">-Force</span></span>
<span data-ttu-id="b1fc6-121">Wymuś usunięcie kontenera i całej jego zawartości</span><span class="sxs-lookup"><span data-stu-id="b1fc6-121">Force to remove the container and all content in it</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1fc6-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b1fc6-122">-InputObject</span></span>
<span data-ttu-id="b1fc6-123">Obiekt kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="b1fc6-123">Storage container object</span></span>

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

### <span data-ttu-id="b1fc6-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b1fc6-124">-Name</span></span>
<span data-ttu-id="b1fc6-125">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="b1fc6-125">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1fc6-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1fc6-126">-PassThru</span></span>
<span data-ttu-id="b1fc6-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b1fc6-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1fc6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1fc6-128">-ResourceGroupName</span></span>
<span data-ttu-id="b1fc6-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b1fc6-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="b1fc6-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b1fc6-130">-StorageAccount</span></span>
<span data-ttu-id="b1fc6-131">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="b1fc6-131">Storage account object</span></span>

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

### <span data-ttu-id="b1fc6-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b1fc6-132">-StorageAccountName</span></span>
<span data-ttu-id="b1fc6-133">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b1fc6-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="b1fc6-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b1fc6-134">-Confirm</span></span>
<span data-ttu-id="b1fc6-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1fc6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1fc6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1fc6-136">-WhatIf</span></span>
<span data-ttu-id="b1fc6-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1fc6-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1fc6-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b1fc6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1fc6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1fc6-139">CommonParameters</span></span>
<span data-ttu-id="b1fc6-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1fc6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1fc6-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1fc6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1fc6-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1fc6-142">INPUTS</span></span>

### <span data-ttu-id="b1fc6-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b1fc6-143">System.String</span></span>

## <span data-ttu-id="b1fc6-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b1fc6-144">OUTPUTS</span></span>

### <span data-ttu-id="b1fc6-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="b1fc6-145">System.Object</span></span>

## <span data-ttu-id="b1fc6-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b1fc6-146">NOTES</span></span>

## <span data-ttu-id="b1fc6-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1fc6-147">RELATED LINKS</span></span>
