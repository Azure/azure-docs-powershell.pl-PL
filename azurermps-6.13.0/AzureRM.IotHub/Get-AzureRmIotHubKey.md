---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
ms.openlocfilehash: 33232e5e8f415309bec36f8918c272c251835f82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552819"
---
# <span data-ttu-id="75335-101">Get-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="75335-101">Get-AzureRmIotHubKey</span></span>

## <span data-ttu-id="75335-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="75335-102">SYNOPSIS</span></span>
<span data-ttu-id="75335-103">Pobiera klucz IotHub.</span><span class="sxs-lookup"><span data-stu-id="75335-103">Gets an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75335-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="75335-104">SYNTAX</span></span>

```
Get-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75335-105">Opis</span><span class="sxs-lookup"><span data-stu-id="75335-105">DESCRIPTION</span></span>
<span data-ttu-id="75335-106">Pobiera klucz IotHub.</span><span class="sxs-lookup"><span data-stu-id="75335-106">Gets an IotHub Key.</span></span>
<span data-ttu-id="75335-107">Możesz wyświetlić listę wszystkich kluczy lub filtrować listę według określonej nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="75335-107">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="75335-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="75335-108">EXAMPLES</span></span>

### <span data-ttu-id="75335-109">Przykład 1 Pobierz wszystkie klucze</span><span class="sxs-lookup"><span data-stu-id="75335-109">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="75335-110">Pobiera wszystkie klucze IotHub o nazwie "myiothub"</span><span class="sxs-lookup"><span data-stu-id="75335-110">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="75335-111">Przykład 2 uzyskiwanie informacji dotyczących określonego klucza</span><span class="sxs-lookup"><span data-stu-id="75335-111">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="75335-112">Pobiera informacje dotyczące klucza o nazwie "iothubowner" dla IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="75335-112">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="75335-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="75335-113">PARAMETERS</span></span>

### <span data-ttu-id="75335-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75335-114">-DefaultProfile</span></span>
<span data-ttu-id="75335-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="75335-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75335-116">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="75335-116">-KeyName</span></span>
<span data-ttu-id="75335-117">Nazwa klucza</span><span class="sxs-lookup"><span data-stu-id="75335-117">Name of the Key</span></span>

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

### <span data-ttu-id="75335-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="75335-118">-Name</span></span>
<span data-ttu-id="75335-119">Nazwa Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="75335-119">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="75335-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75335-120">-ResourceGroupName</span></span>
<span data-ttu-id="75335-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="75335-121">Resource Group Name</span></span>

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

### <span data-ttu-id="75335-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75335-122">CommonParameters</span></span>
<span data-ttu-id="75335-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75335-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75335-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75335-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75335-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75335-125">INPUTS</span></span>

### <span data-ttu-id="75335-126">System. String</span><span class="sxs-lookup"><span data-stu-id="75335-126">System.String</span></span>

## <span data-ttu-id="75335-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="75335-127">OUTPUTS</span></span>

### <span data-ttu-id="75335-128">Microsoft. Azure. Commands. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="75335-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="75335-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="75335-129">NOTES</span></span>

## <span data-ttu-id="75335-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75335-130">RELATED LINKS</span></span>
