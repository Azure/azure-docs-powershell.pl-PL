---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: 5463c20274f60c2d6fb6c4807bf2c4d27da76808
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707459"
---
# <span data-ttu-id="4fe5d-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="4fe5d-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="4fe5d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4fe5d-102">SYNOPSIS</span></span>
<span data-ttu-id="4fe5d-103">To polecenie ponownie wywołuje wszystkie pliki warstw z powrotem na dysk lokalny.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="4fe5d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4fe5d-104">SYNTAX</span></span>

### <span data-ttu-id="4fe5d-105">ObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4fe5d-105">ObjectParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fe5d-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fe5d-106">StringParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fe5d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fe5d-107">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fe5d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4fe5d-108">DESCRIPTION</span></span>
<span data-ttu-id="4fe5d-109">Jeśli w punkcie końcowym serwera (określona lokalizacja na zarejestrowanego serwera) włączono funkcję warstw chmury, za pomocą tego polecenia można odwołać wszystkie pliki warstwowe do dysku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="4fe5d-110">Zdecydowanie zaleca się wyłączenie warstw chmury na tym punkcie końcowym serwera przed rozpoczęciem odwołania.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="4fe5d-111">Jeśli poziom napełnienia warstw jest nadal włączony, funkcja odwoływania może prowadzić do innych plików, które nie mają na celu osiągnięcia odpowiedniego celu całej zawartości znajdującej się na dysku lokalnym.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="4fe5d-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4fe5d-112">EXAMPLES</span></span>

### <span data-ttu-id="4fe5d-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4fe5d-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="4fe5d-114">To polecenie rekurencyjnie odwołuje wszystkie pliki warstwowe znajdujące się w ścieżce katalogu głównego określonego punktu końcowego serwera.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="4fe5d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4fe5d-115">PARAMETERS</span></span>

### <span data-ttu-id="4fe5d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4fe5d-116">-AsJob</span></span>
<span data-ttu-id="4fe5d-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4fe5d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4fe5d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fe5d-118">-DefaultProfile</span></span>
<span data-ttu-id="4fe5d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fe5d-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4fe5d-120">-InputObject</span></span>
<span data-ttu-id="4fe5d-121">Obiekt do synchronizacji, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-121">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fe5d-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4fe5d-122">-Name</span></span>
<span data-ttu-id="4fe5d-123">Nazwa ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-123">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="4fe5d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fe5d-124">-PassThru</span></span>
<span data-ttu-id="4fe5d-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4fe5d-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4fe5d-126">-Wzorzec</span><span class="sxs-lookup"><span data-stu-id="4fe5d-126">-Pattern</span></span>
<span data-ttu-id="4fe5d-127">Wzorzec nazwy pliku</span><span class="sxs-lookup"><span data-stu-id="4fe5d-127">Pattern of the file name</span></span>

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

### <span data-ttu-id="4fe5d-128">-RecallPath</span><span class="sxs-lookup"><span data-stu-id="4fe5d-128">-RecallPath</span></span>
<span data-ttu-id="4fe5d-129">Ścieżka odwołania, która musi zostać odwołana.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-129">Recall path which need to be recalled.</span></span>

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

### <span data-ttu-id="4fe5d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fe5d-130">-ResourceGroupName</span></span>
<span data-ttu-id="4fe5d-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="4fe5d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fe5d-132">-ResourceId</span></span>
<span data-ttu-id="4fe5d-133">Identyfikator zasobu ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4fe5d-133">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="4fe5d-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="4fe5d-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="4fe5d-135">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-135">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="4fe5d-136">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="4fe5d-136">-SyncGroupName</span></span>
<span data-ttu-id="4fe5d-137">Nazwa tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-137">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="4fe5d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fe5d-138">CommonParameters</span></span>
<span data-ttu-id="4fe5d-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fe5d-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fe5d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fe5d-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4fe5d-141">INPUTS</span></span>

### <span data-ttu-id="4fe5d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4fe5d-142">System.String</span></span>

### <span data-ttu-id="4fe5d-143">Microsoft. Azure. Commands. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4fe5d-143">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="4fe5d-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4fe5d-144">OUTPUTS</span></span>

### <span data-ttu-id="4fe5d-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4fe5d-145">System.Boolean</span></span>

## <span data-ttu-id="4fe5d-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4fe5d-146">NOTES</span></span>

## <span data-ttu-id="4fe5d-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4fe5d-147">RELATED LINKS</span></span>
