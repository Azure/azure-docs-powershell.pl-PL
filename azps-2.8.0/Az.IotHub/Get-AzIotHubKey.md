---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: c38965a99dfc152f76e606c05802009b9b14faf9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705242"
---
# <span data-ttu-id="373ac-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="373ac-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="373ac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="373ac-102">SYNOPSIS</span></span>
<span data-ttu-id="373ac-103">Pobiera klucz IotHub.</span><span class="sxs-lookup"><span data-stu-id="373ac-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="373ac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="373ac-104">SYNTAX</span></span>

### <span data-ttu-id="373ac-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="373ac-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="373ac-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="373ac-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="373ac-107">Opis</span><span class="sxs-lookup"><span data-stu-id="373ac-107">DESCRIPTION</span></span>
<span data-ttu-id="373ac-108">Pobiera klucz IotHub.</span><span class="sxs-lookup"><span data-stu-id="373ac-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="373ac-109">Możesz wyświetlić listę wszystkich kluczy lub filtrować listę według określonej nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="373ac-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="373ac-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="373ac-110">EXAMPLES</span></span>

### <span data-ttu-id="373ac-111">Przykład 1 Pobierz wszystkie klucze</span><span class="sxs-lookup"><span data-stu-id="373ac-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="373ac-112">Pobiera wszystkie klucze IotHub o nazwie "myiothub"</span><span class="sxs-lookup"><span data-stu-id="373ac-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="373ac-113">Przykład 2 uzyskiwanie informacji dotyczących określonego klucza</span><span class="sxs-lookup"><span data-stu-id="373ac-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="373ac-114">Pobiera informacje dotyczące klucza o nazwie "iothubowner" dla IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="373ac-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="373ac-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="373ac-115">PARAMETERS</span></span>

### <span data-ttu-id="373ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="373ac-116">-DefaultProfile</span></span>
<span data-ttu-id="373ac-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="373ac-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="373ac-118">-HubId</span><span class="sxs-lookup"><span data-stu-id="373ac-118">-HubId</span></span>
<span data-ttu-id="373ac-119">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="373ac-119">IotHub Resource Id</span></span>

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

### <span data-ttu-id="373ac-120">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="373ac-120">-KeyName</span></span>
<span data-ttu-id="373ac-121">Nazwa klucza</span><span class="sxs-lookup"><span data-stu-id="373ac-121">Name of the Key</span></span>

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

### <span data-ttu-id="373ac-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="373ac-122">-Name</span></span>
<span data-ttu-id="373ac-123">Nazwa Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="373ac-123">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="373ac-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="373ac-124">-ResourceGroupName</span></span>
<span data-ttu-id="373ac-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="373ac-125">Resource Group Name</span></span>

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

### <span data-ttu-id="373ac-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="373ac-126">CommonParameters</span></span>
<span data-ttu-id="373ac-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="373ac-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="373ac-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="373ac-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="373ac-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="373ac-129">INPUTS</span></span>

### <span data-ttu-id="373ac-130">System. String</span><span class="sxs-lookup"><span data-stu-id="373ac-130">System.String</span></span>

## <span data-ttu-id="373ac-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="373ac-131">OUTPUTS</span></span>

### <span data-ttu-id="373ac-132">Microsoft. Azure. Commands. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="373ac-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="373ac-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="373ac-133">NOTES</span></span>

## <span data-ttu-id="373ac-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="373ac-134">RELATED LINKS</span></span>
