---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
ms.openlocfilehash: ef4ac5058c1ce85e19a9854bcd11fc2fac5ac69e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545684"
---
# <span data-ttu-id="6750a-101">Get-AzureRmIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="6750a-101">Get-AzureRmIotHubConnectionString</span></span>

## <span data-ttu-id="6750a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6750a-102">SYNOPSIS</span></span>
<span data-ttu-id="6750a-103">Pobiera connectionStrings IotHub.</span><span class="sxs-lookup"><span data-stu-id="6750a-103">Gets the IotHub connectionstrings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6750a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6750a-104">SYNTAX</span></span>

```
Get-AzureRmIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6750a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6750a-105">DESCRIPTION</span></span>
<span data-ttu-id="6750a-106">Pobiera connectionStrings IotHub.</span><span class="sxs-lookup"><span data-stu-id="6750a-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="6750a-107">Możesz pobrać connectionStrings dla wszystkich kluczy lub filtrować je według określonej nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="6750a-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="6750a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6750a-108">EXAMPLES</span></span>

### <span data-ttu-id="6750a-109">Przykład 1 Pobierz wszystkie IotHub connectionStrings</span><span class="sxs-lookup"><span data-stu-id="6750a-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="6750a-110">Pobiera connectionStrings dla wszystkich kluczy iothub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="6750a-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="6750a-111">Przykład 2 uzyskiwanie connectionStrings IotHub dla określonego klucza</span><span class="sxs-lookup"><span data-stu-id="6750a-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="6750a-112">Pobiera connectionStrings dla klucza o nazwie "MyKey" dla iothub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="6750a-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="6750a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6750a-113">PARAMETERS</span></span>

### <span data-ttu-id="6750a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6750a-114">-DefaultProfile</span></span>
<span data-ttu-id="6750a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6750a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6750a-116">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="6750a-116">-KeyName</span></span>
<span data-ttu-id="6750a-117">Nazwa klucza</span><span class="sxs-lookup"><span data-stu-id="6750a-117">Name of the Key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6750a-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6750a-118">-Name</span></span>
<span data-ttu-id="6750a-119">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="6750a-119">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6750a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6750a-120">-ResourceGroupName</span></span>
<span data-ttu-id="6750a-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6750a-121">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6750a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6750a-122">CommonParameters</span></span>
<span data-ttu-id="6750a-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6750a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6750a-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6750a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6750a-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6750a-125">INPUTS</span></span>

### <span data-ttu-id="6750a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6750a-126">System.String</span></span>

## <span data-ttu-id="6750a-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6750a-127">OUTPUTS</span></span>

### <span data-ttu-id="6750a-128">Microsoft. Azure. Commands. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6750a-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="6750a-129">System. Collections. Generic. list \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. MODELES. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral; PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="6750a-129">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="6750a-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6750a-130">NOTES</span></span>

## <span data-ttu-id="6750a-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6750a-131">RELATED LINKS</span></span>

