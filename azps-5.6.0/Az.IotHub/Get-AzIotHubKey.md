---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: 4a63f13e567a5f53726058c831107ce43768c0f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987974"
---
# <span data-ttu-id="e3f39-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="e3f39-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="e3f39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3f39-102">SYNOPSIS</span></span>
<span data-ttu-id="e3f39-103">Pobiera klucz aplikacji IotHub.</span><span class="sxs-lookup"><span data-stu-id="e3f39-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="e3f39-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e3f39-104">SYNTAX</span></span>

### <span data-ttu-id="e3f39-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e3f39-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3f39-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e3f39-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3f39-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e3f39-107">DESCRIPTION</span></span>
<span data-ttu-id="e3f39-108">Pobiera klucz aplikacji IotHub.</span><span class="sxs-lookup"><span data-stu-id="e3f39-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="e3f39-109">Możesz wyświetlić listę wszystkich kluczy lub przefiltrować listę według konkretnej nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="e3f39-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="e3f39-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e3f39-110">EXAMPLES</span></span>

### <span data-ttu-id="e3f39-111">Przykład 1. Uzyskiwanie wszystkich kluczy</span><span class="sxs-lookup"><span data-stu-id="e3f39-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="e3f39-112">Pobiera wszystkie klucze dla usługi IotHub o nazwie "myiothub"</span><span class="sxs-lookup"><span data-stu-id="e3f39-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="e3f39-113">Przykład 2. Uzyskiwanie informacji dotyczących określonego klucza</span><span class="sxs-lookup"><span data-stu-id="e3f39-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="e3f39-114">Pobiera informacje dotyczące klucza o nazwie "iothubowner" dla usługi IotHub o nazwie "myiothub"</span><span class="sxs-lookup"><span data-stu-id="e3f39-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="e3f39-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3f39-115">PARAMETERS</span></span>

### <span data-ttu-id="e3f39-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3f39-116">-DefaultProfile</span></span>
<span data-ttu-id="e3f39-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e3f39-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3f39-118">— HubId</span><span class="sxs-lookup"><span data-stu-id="e3f39-118">-HubId</span></span>
<span data-ttu-id="e3f39-119">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="e3f39-119">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f39-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e3f39-120">-KeyName</span></span>
<span data-ttu-id="e3f39-121">Nazwa klucza</span><span class="sxs-lookup"><span data-stu-id="e3f39-121">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3f39-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e3f39-122">-Name</span></span>
<span data-ttu-id="e3f39-123">Nazwa centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="e3f39-123">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f39-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3f39-124">-ResourceGroupName</span></span>
<span data-ttu-id="e3f39-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e3f39-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f39-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3f39-126">CommonParameters</span></span>
<span data-ttu-id="e3f39-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3f39-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3f39-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3f39-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3f39-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3f39-129">INPUTS</span></span>

### <span data-ttu-id="e3f39-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e3f39-130">System.String</span></span>

## <span data-ttu-id="e3f39-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3f39-131">OUTPUTS</span></span>

### <span data-ttu-id="e3f39-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e3f39-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="e3f39-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e3f39-133">NOTES</span></span>

## <span data-ttu-id="e3f39-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3f39-134">RELATED LINKS</span></span>
