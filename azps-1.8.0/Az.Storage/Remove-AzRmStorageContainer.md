---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
ms.openlocfilehash: d7a4563a32da28215dbb9b6dab2b911a500183a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707553"
---
# <span data-ttu-id="c7a5f-101">Remove-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c7a5f-101">Remove-AzRmStorageContainer</span></span>

## <span data-ttu-id="c7a5f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c7a5f-102">SYNOPSIS</span></span>
<span data-ttu-id="c7a5f-103">Usuwa kontener obiektu blob magazynu</span><span class="sxs-lookup"><span data-stu-id="c7a5f-103">Removes a Storage blob container</span></span>

## <span data-ttu-id="c7a5f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c7a5f-104">SYNTAX</span></span>

### <span data-ttu-id="c7a5f-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="c7a5f-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7a5f-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="c7a5f-106">AccountObject</span></span>
```
Remove-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7a5f-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="c7a5f-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7a5f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c7a5f-108">DESCRIPTION</span></span>
<span data-ttu-id="c7a5f-109">Polecenie cmdlet **Remove-AzRmStorageContainer** usuwa kontener obiektu BLOB magazynowania</span><span class="sxs-lookup"><span data-stu-id="c7a5f-109">The **Remove-AzRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="c7a5f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c7a5f-110">EXAMPLES</span></span>

### <span data-ttu-id="c7a5f-111">Przykład 1. Usuń kontener obiektu blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="c7a5f-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="c7a5f-112">To polecenie usuwa kontener obiektu blob magazynu z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="c7a5f-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="c7a5f-113">Przykład 2: usuwanie kontenera obiektu blob magazynu z obiektem konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="c7a5f-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="c7a5f-114">To polecenie usuwa kontener obiektu blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="c7a5f-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="c7a5f-115">Przykład 3: Usuwanie wszystkich kontenerów obiektów blob magazynu na koncie magazynu z potokiem</span><span class="sxs-lookup"><span data-stu-id="c7a5f-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainer -Force
```

<span data-ttu-id="c7a5f-116">To polecenie usuwa wszystkie kontenery obiektów blob magazynu z konta magazynu z potokiem.</span><span class="sxs-lookup"><span data-stu-id="c7a5f-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="c7a5f-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c7a5f-117">PARAMETERS</span></span>

### <span data-ttu-id="c7a5f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7a5f-118">-DefaultProfile</span></span>
<span data-ttu-id="c7a5f-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c7a5f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7a5f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c7a5f-120">-Force</span></span>
<span data-ttu-id="c7a5f-121">Wymuś usunięcie kontenera i całej jego zawartości</span><span class="sxs-lookup"><span data-stu-id="c7a5f-121">Force to remove the container and all content in it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a5f-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c7a5f-122">-InputObject</span></span>
<span data-ttu-id="c7a5f-123">Obiekt kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="c7a5f-123">Storage container object</span></span>

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

### <span data-ttu-id="c7a5f-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c7a5f-124">-Name</span></span>
<span data-ttu-id="c7a5f-125">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="c7a5f-125">Container Name</span></span>

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

### <span data-ttu-id="c7a5f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7a5f-126">-PassThru</span></span>
<span data-ttu-id="c7a5f-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c7a5f-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a5f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7a5f-128">-ResourceGroupName</span></span>
<span data-ttu-id="c7a5f-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c7a5f-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="c7a5f-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c7a5f-130">-StorageAccount</span></span>
<span data-ttu-id="c7a5f-131">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="c7a5f-131">Storage account object</span></span>

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

### <span data-ttu-id="c7a5f-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c7a5f-132">-StorageAccountName</span></span>
<span data-ttu-id="c7a5f-133">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="c7a5f-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="c7a5f-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c7a5f-134">-Confirm</span></span>
<span data-ttu-id="c7a5f-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7a5f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7a5f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7a5f-136">-WhatIf</span></span>
<span data-ttu-id="c7a5f-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7a5f-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7a5f-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c7a5f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7a5f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7a5f-139">CommonParameters</span></span>
<span data-ttu-id="c7a5f-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7a5f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7a5f-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7a5f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7a5f-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7a5f-142">INPUTS</span></span>

### <span data-ttu-id="c7a5f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c7a5f-143">System.String</span></span>

### <span data-ttu-id="c7a5f-144">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c7a5f-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="c7a5f-145">Microsoft. Azure. Commands. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="c7a5f-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="c7a5f-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c7a5f-146">OUTPUTS</span></span>

### <span data-ttu-id="c7a5f-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c7a5f-147">System.Boolean</span></span>

## <span data-ttu-id="c7a5f-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c7a5f-148">NOTES</span></span>

## <span data-ttu-id="c7a5f-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c7a5f-149">RELATED LINKS</span></span>
