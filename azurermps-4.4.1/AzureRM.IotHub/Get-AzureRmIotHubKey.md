---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
ms.openlocfilehash: db2cf6c9daae5b96642a6408b990276feffc8598
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550983"
---
# <span data-ttu-id="120b5-101">Get-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="120b5-101">Get-AzureRmIotHubKey</span></span>

## <span data-ttu-id="120b5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="120b5-102">SYNOPSIS</span></span>
<span data-ttu-id="120b5-103">Pobiera klucz IotHub.</span><span class="sxs-lookup"><span data-stu-id="120b5-103">Gets an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="120b5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="120b5-104">SYNTAX</span></span>

```
Get-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="120b5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="120b5-105">DESCRIPTION</span></span>
<span data-ttu-id="120b5-106">Pobiera klucz IotHub.</span><span class="sxs-lookup"><span data-stu-id="120b5-106">Gets an IotHub Key.</span></span>
<span data-ttu-id="120b5-107">Możesz wyświetlić listę wszystkich kluczy lub filtrować listę według określonej nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="120b5-107">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="120b5-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="120b5-108">EXAMPLES</span></span>

### <span data-ttu-id="120b5-109">Przykład 1 Pobierz wszystkie klucze</span><span class="sxs-lookup"><span data-stu-id="120b5-109">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="120b5-110">Pobiera wszystkie klucze IotHub o nazwie "myiothub"</span><span class="sxs-lookup"><span data-stu-id="120b5-110">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="120b5-111">Przykład 2 uzyskiwanie informacji dotyczących określonego klucza</span><span class="sxs-lookup"><span data-stu-id="120b5-111">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="120b5-112">Pobiera informacje dotyczące klucza o nazwie "iothubowner" dla IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="120b5-112">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="120b5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="120b5-113">PARAMETERS</span></span>

### <span data-ttu-id="120b5-114">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="120b5-114">-KeyName</span></span>
<span data-ttu-id="120b5-115">Nazwa klucza</span><span class="sxs-lookup"><span data-stu-id="120b5-115">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120b5-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="120b5-116">-Name</span></span>
<span data-ttu-id="120b5-117">Nazwa Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="120b5-117">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="120b5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="120b5-118">-ResourceGroupName</span></span>
<span data-ttu-id="120b5-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="120b5-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="120b5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="120b5-120">-DefaultProfile</span></span>
<span data-ttu-id="120b5-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="120b5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120b5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="120b5-122">CommonParameters</span></span>
<span data-ttu-id="120b5-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="120b5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="120b5-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="120b5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="120b5-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="120b5-125">INPUTS</span></span>

### <span data-ttu-id="120b5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="120b5-126">System.String</span></span>

## <span data-ttu-id="120b5-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="120b5-127">OUTPUTS</span></span>

### <span data-ttu-id="120b5-128">Microsoft. Azure. Commands. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="120b5-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="120b5-129">System. Collections. Generic. list \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. MODELES. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral; PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="120b5-129">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="120b5-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="120b5-130">NOTES</span></span>

## <span data-ttu-id="120b5-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="120b5-131">RELATED LINKS</span></span>

