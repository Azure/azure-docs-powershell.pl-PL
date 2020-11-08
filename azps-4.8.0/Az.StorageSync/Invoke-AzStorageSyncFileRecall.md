---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: fb053da61aabd9328f4ff3d848243ff9b84d6d09
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219706"
---
# <span data-ttu-id="b93f7-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="b93f7-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="b93f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b93f7-102">SYNOPSIS</span></span>
<span data-ttu-id="b93f7-103">To polecenie ponownie wywołuje wszystkie pliki warstw z powrotem na dysk lokalny.</span><span class="sxs-lookup"><span data-stu-id="b93f7-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="b93f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b93f7-104">SYNTAX</span></span>

### <span data-ttu-id="b93f7-105">StringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b93f7-105">StringParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b93f7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b93f7-106">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b93f7-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b93f7-107">ObjectParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b93f7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b93f7-108">DESCRIPTION</span></span>
<span data-ttu-id="b93f7-109">Jeśli w punkcie końcowym serwera (określona lokalizacja na zarejestrowanego serwera) włączono funkcję warstw chmury, za pomocą tego polecenia można odwołać wszystkie pliki warstwowe do dysku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="b93f7-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="b93f7-110">Zdecydowanie zaleca się wyłączenie warstw chmury na tym punkcie końcowym serwera przed rozpoczęciem odwołania.</span><span class="sxs-lookup"><span data-stu-id="b93f7-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="b93f7-111">Jeśli poziom napełnienia warstw jest nadal włączony, funkcja odwoływania może prowadzić do innych plików, które nie mają na celu osiągnięcia odpowiedniego celu całej zawartości znajdującej się na dysku lokalnym.</span><span class="sxs-lookup"><span data-stu-id="b93f7-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="b93f7-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b93f7-112">EXAMPLES</span></span>

### <span data-ttu-id="b93f7-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b93f7-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="b93f7-114">To polecenie rekurencyjnie odwołuje wszystkie pliki warstwowe znajdujące się w ścieżce katalogu głównego określonego punktu końcowego serwera.</span><span class="sxs-lookup"><span data-stu-id="b93f7-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="b93f7-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b93f7-115">PARAMETERS</span></span>

### <span data-ttu-id="b93f7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b93f7-116">-AsJob</span></span>
<span data-ttu-id="b93f7-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b93f7-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b93f7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b93f7-118">-DefaultProfile</span></span>
<span data-ttu-id="b93f7-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b93f7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b93f7-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b93f7-120">-InputObject</span></span>
<span data-ttu-id="b93f7-121">Obiekt do synchronizacji, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="b93f7-121">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer, ServerEndpoint

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b93f7-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b93f7-122">-Name</span></span>
<span data-ttu-id="b93f7-123">Nazwa ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="b93f7-123">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ServerEndpointName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93f7-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b93f7-124">-PassThru</span></span>
<span data-ttu-id="b93f7-125">W przypadku normalnego wykonywania to polecenie cmdlet nie zwraca żadnej wartości po powodzeniu.</span><span class="sxs-lookup"><span data-stu-id="b93f7-125">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="b93f7-126">Jeśli podasz parametr PassThru, polecenie cmdlet nastąpi wartość do rurociągu po poprawnym wykonaniu.</span><span class="sxs-lookup"><span data-stu-id="b93f7-126">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="b93f7-127">-Wzorzec</span><span class="sxs-lookup"><span data-stu-id="b93f7-127">-Pattern</span></span>
<span data-ttu-id="b93f7-128">Wzorzec nazwy pliku</span><span class="sxs-lookup"><span data-stu-id="b93f7-128">Pattern of the file name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93f7-129">-RecallPath</span><span class="sxs-lookup"><span data-stu-id="b93f7-129">-RecallPath</span></span>
<span data-ttu-id="b93f7-130">Ścieżka odwołania, która musi zostać odwołana.</span><span class="sxs-lookup"><span data-stu-id="b93f7-130">Recall path which need to be recalled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93f7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b93f7-131">-ResourceGroupName</span></span>
<span data-ttu-id="b93f7-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b93f7-132">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93f7-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b93f7-133">-ResourceId</span></span>
<span data-ttu-id="b93f7-134">Identyfikator zasobu ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b93f7-134">ServerEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b93f7-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="b93f7-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="b93f7-136">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="b93f7-136">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93f7-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="b93f7-137">-SyncGroupName</span></span>
<span data-ttu-id="b93f7-138">Nazwa tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="b93f7-138">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93f7-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b93f7-139">-Confirm</span></span>
<span data-ttu-id="b93f7-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b93f7-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b93f7-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b93f7-141">-WhatIf</span></span>
<span data-ttu-id="b93f7-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b93f7-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b93f7-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b93f7-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b93f7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b93f7-144">CommonParameters</span></span>
<span data-ttu-id="b93f7-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b93f7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b93f7-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b93f7-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b93f7-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b93f7-147">INPUTS</span></span>

### <span data-ttu-id="b93f7-148">System. String</span><span class="sxs-lookup"><span data-stu-id="b93f7-148">System.String</span></span>

### <span data-ttu-id="b93f7-149">Microsoft. Azure. Commands. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b93f7-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="b93f7-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b93f7-150">OUTPUTS</span></span>

### <span data-ttu-id="b93f7-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b93f7-151">System.Boolean</span></span>

## <span data-ttu-id="b93f7-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b93f7-152">NOTES</span></span>

## <span data-ttu-id="b93f7-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b93f7-153">RELATED LINKS</span></span>
