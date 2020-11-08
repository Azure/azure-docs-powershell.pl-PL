---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: 258d1e1bad9eca1fd8817e1eaa499eb5bc3d8d49
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223887"
---
# <span data-ttu-id="774a5-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="774a5-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="774a5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="774a5-102">SYNOPSIS</span></span>
<span data-ttu-id="774a5-103">Pobiera klucz IotHub.</span><span class="sxs-lookup"><span data-stu-id="774a5-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="774a5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="774a5-104">SYNTAX</span></span>

### <span data-ttu-id="774a5-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="774a5-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="774a5-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="774a5-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="774a5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="774a5-107">DESCRIPTION</span></span>
<span data-ttu-id="774a5-108">Pobiera klucz IotHub.</span><span class="sxs-lookup"><span data-stu-id="774a5-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="774a5-109">Możesz wyświetlić listę wszystkich kluczy lub filtrować listę według określonej nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="774a5-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="774a5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="774a5-110">EXAMPLES</span></span>

### <span data-ttu-id="774a5-111">Przykład 1 Pobierz wszystkie klucze</span><span class="sxs-lookup"><span data-stu-id="774a5-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="774a5-112">Pobiera wszystkie klucze IotHub o nazwie "myiothub"</span><span class="sxs-lookup"><span data-stu-id="774a5-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="774a5-113">Przykład 2 uzyskiwanie informacji dotyczących określonego klucza</span><span class="sxs-lookup"><span data-stu-id="774a5-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="774a5-114">Pobiera informacje dotyczące klucza o nazwie "iothubowner" dla IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="774a5-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="774a5-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="774a5-115">PARAMETERS</span></span>

### <span data-ttu-id="774a5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="774a5-116">-DefaultProfile</span></span>
<span data-ttu-id="774a5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="774a5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="774a5-118">-HubId</span><span class="sxs-lookup"><span data-stu-id="774a5-118">-HubId</span></span>
<span data-ttu-id="774a5-119">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="774a5-119">IotHub Resource Id</span></span>

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

### <span data-ttu-id="774a5-120">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="774a5-120">-KeyName</span></span>
<span data-ttu-id="774a5-121">Nazwa klucza</span><span class="sxs-lookup"><span data-stu-id="774a5-121">Name of the Key</span></span>

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

### <span data-ttu-id="774a5-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="774a5-122">-Name</span></span>
<span data-ttu-id="774a5-123">Nazwa Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="774a5-123">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="774a5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="774a5-124">-ResourceGroupName</span></span>
<span data-ttu-id="774a5-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="774a5-125">Resource Group Name</span></span>

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

### <span data-ttu-id="774a5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="774a5-126">CommonParameters</span></span>
<span data-ttu-id="774a5-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="774a5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="774a5-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="774a5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="774a5-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="774a5-129">INPUTS</span></span>

### <span data-ttu-id="774a5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="774a5-130">System.String</span></span>

## <span data-ttu-id="774a5-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="774a5-131">OUTPUTS</span></span>

### <span data-ttu-id="774a5-132">Microsoft. Azure. Commands. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="774a5-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="774a5-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="774a5-133">NOTES</span></span>

## <span data-ttu-id="774a5-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="774a5-134">RELATED LINKS</span></span>
