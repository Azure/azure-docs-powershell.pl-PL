---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: f84d233280bc771b90f47c5769fdb6d3f35c2e0c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232227"
---
# <span data-ttu-id="0b714-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="0b714-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="0b714-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0b714-102">SYNOPSIS</span></span>
<span data-ttu-id="0b714-103">Pobiera connectionStrings IotHub.</span><span class="sxs-lookup"><span data-stu-id="0b714-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="0b714-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0b714-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b714-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0b714-105">DESCRIPTION</span></span>
<span data-ttu-id="0b714-106">Pobiera connectionStrings IotHub.</span><span class="sxs-lookup"><span data-stu-id="0b714-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="0b714-107">Możesz pobrać connectionStrings dla wszystkich kluczy lub filtrować je według określonej nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="0b714-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="0b714-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0b714-108">EXAMPLES</span></span>

### <span data-ttu-id="0b714-109">Przykład 1 Pobierz wszystkie IotHub connectionStrings</span><span class="sxs-lookup"><span data-stu-id="0b714-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="0b714-110">Pobiera connectionStrings dla wszystkich kluczy iothub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="0b714-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="0b714-111">Przykład 2 uzyskiwanie connectionStrings IotHub dla określonego klucza</span><span class="sxs-lookup"><span data-stu-id="0b714-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="0b714-112">Pobiera connectionStrings dla klucza o nazwie "MyKey" dla iothub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="0b714-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="0b714-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0b714-113">PARAMETERS</span></span>

### <span data-ttu-id="0b714-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b714-114">-DefaultProfile</span></span>
<span data-ttu-id="0b714-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0b714-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b714-116">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="0b714-116">-KeyName</span></span>
<span data-ttu-id="0b714-117">Nazwa klucza</span><span class="sxs-lookup"><span data-stu-id="0b714-117">Name of the Key</span></span>

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

### <span data-ttu-id="0b714-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0b714-118">-Name</span></span>
<span data-ttu-id="0b714-119">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="0b714-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="0b714-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b714-120">-ResourceGroupName</span></span>
<span data-ttu-id="0b714-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0b714-121">Resource Group Name</span></span>

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

### <span data-ttu-id="0b714-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b714-122">CommonParameters</span></span>
<span data-ttu-id="0b714-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b714-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b714-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b714-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b714-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b714-125">INPUTS</span></span>

### <span data-ttu-id="0b714-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0b714-126">System.String</span></span>

## <span data-ttu-id="0b714-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0b714-127">OUTPUTS</span></span>

### <span data-ttu-id="0b714-128">Microsoft. Azure. Commands. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0b714-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="0b714-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0b714-129">NOTES</span></span>

## <span data-ttu-id="0b714-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b714-130">RELATED LINKS</span></span>
