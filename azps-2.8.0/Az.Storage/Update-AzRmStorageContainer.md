---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
ms.openlocfilehash: 879645975636a981ded22a0fe63d398fc4659d85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887797"
---
# <span data-ttu-id="2c119-101">Update-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2c119-101">Update-AzRmStorageContainer</span></span>

## <span data-ttu-id="2c119-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c119-102">SYNOPSIS</span></span>
<span data-ttu-id="2c119-103">Modyfikuje kontener obiektu BLOB przechowywania</span><span class="sxs-lookup"><span data-stu-id="2c119-103">Modifies a Storage blob container</span></span>

## <span data-ttu-id="2c119-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c119-104">SYNTAX</span></span>

### <span data-ttu-id="2c119-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="2c119-105">AccountName (Default)</span></span>
```
Update-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c119-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="2c119-106">AccountObject</span></span>
```
Update-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c119-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="2c119-107">ContainerObject</span></span>
```
Update-AzRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c119-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2c119-108">DESCRIPTION</span></span>
<span data-ttu-id="2c119-109">Polecenie cmdlet **Update-AzRmStorageContainer** modyfikuje kontener obiektu BLOB przechowywania</span><span class="sxs-lookup"><span data-stu-id="2c119-109">The **Update-AzRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="2c119-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c119-110">EXAMPLES</span></span>

### <span data-ttu-id="2c119-111">Przykład 1: modyfikuje metadane kontenera obiektu blob magazynu i dostęp publiczny przy użyciu nazwy konta magazynu i nazwy kontenera</span><span class="sxs-lookup"><span data-stu-id="2c119-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="2c119-112">To polecenie modyfikuje metadane kontenera obiektów blob magazynu i dostęp publiczny przy użyciu nazwy konta magazynu i nazwy kontenera.</span><span class="sxs-lookup"><span data-stu-id="2c119-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="2c119-113">Przykład 2: wyłączanie dostępu publicznego w kontenerze obiektu blob magazynu przy użyciu obiektu konta magazynu i nazwy kontenera</span><span class="sxs-lookup"><span data-stu-id="2c119-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="2c119-114">To polecenie wyłącza dostęp publiczny w kontenerze obiektu blob magazynu przy użyciu obiektu konta magazynu i nazwy kontenera.</span><span class="sxs-lookup"><span data-stu-id="2c119-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="2c119-115">Przykład 3: Ustawianie dostępu publicznego jako obiektu BLOB dla wszystkich kontenerów obiektów blob magazynu na koncie magazynu z potokiem</span><span class="sxs-lookup"><span data-stu-id="2c119-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="2c119-116">To polecenie ustawia dostęp publiczny jako obiekt BLOB dla wszystkich kontenerów blob magazynu na koncie magazynu z potokiem.</span><span class="sxs-lookup"><span data-stu-id="2c119-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="2c119-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c119-117">PARAMETERS</span></span>

### <span data-ttu-id="2c119-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c119-118">-DefaultProfile</span></span>
<span data-ttu-id="2c119-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2c119-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c119-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2c119-120">-InputObject</span></span>
<span data-ttu-id="2c119-121">Obiekt kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="2c119-121">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c119-122">-Metadata</span><span class="sxs-lookup"><span data-stu-id="2c119-122">-Metadata</span></span>
<span data-ttu-id="2c119-123">Metadane kontenera</span><span class="sxs-lookup"><span data-stu-id="2c119-123">Container Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c119-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2c119-124">-Name</span></span>
<span data-ttu-id="2c119-125">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="2c119-125">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c119-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="2c119-126">-PublicAccess</span></span>
<span data-ttu-id="2c119-127">Kontener PublicAccess</span><span class="sxs-lookup"><span data-stu-id="2c119-127">Container PublicAccess</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSPublicAccess
Parameter Sets: (All)
Aliases:
Accepted values: Container, Blob, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c119-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c119-128">-ResourceGroupName</span></span>
<span data-ttu-id="2c119-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2c119-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c119-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c119-130">-StorageAccount</span></span>
<span data-ttu-id="2c119-131">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="2c119-131">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c119-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2c119-132">-StorageAccountName</span></span>
<span data-ttu-id="2c119-133">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="2c119-133">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c119-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2c119-134">-Confirm</span></span>
<span data-ttu-id="2c119-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c119-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c119-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c119-136">-WhatIf</span></span>
<span data-ttu-id="2c119-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c119-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c119-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2c119-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c119-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c119-139">CommonParameters</span></span>
<span data-ttu-id="2c119-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c119-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c119-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c119-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c119-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c119-142">INPUTS</span></span>

### <span data-ttu-id="2c119-143">System. String</span><span class="sxs-lookup"><span data-stu-id="2c119-143">System.String</span></span>

### <span data-ttu-id="2c119-144">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c119-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="2c119-145">Microsoft. Azure. Commands. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="2c119-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="2c119-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c119-146">OUTPUTS</span></span>

### <span data-ttu-id="2c119-147">Microsoft. Azure. Commands. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="2c119-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="2c119-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c119-148">NOTES</span></span>

## <span data-ttu-id="2c119-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c119-149">RELATED LINKS</span></span>
