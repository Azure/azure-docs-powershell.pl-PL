---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
ms.openlocfilehash: 52c5bee4e699ff063794f140ce4360669180a164
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718197"
---
# <span data-ttu-id="62ba7-101">Get-AzureRmIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="62ba7-101">Get-AzureRmIotHubConnectionString</span></span>

## <span data-ttu-id="62ba7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="62ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="62ba7-103">Pobiera connectionStrings IotHub.</span><span class="sxs-lookup"><span data-stu-id="62ba7-103">Gets the IotHub connectionstrings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62ba7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="62ba7-104">SYNTAX</span></span>

```
Get-AzureRmIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62ba7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="62ba7-105">DESCRIPTION</span></span>
<span data-ttu-id="62ba7-106">Pobiera connectionStrings IotHub.</span><span class="sxs-lookup"><span data-stu-id="62ba7-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="62ba7-107">Możesz pobrać connectionStrings dla wszystkich kluczy lub filtrować je według określonej nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="62ba7-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="62ba7-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="62ba7-108">EXAMPLES</span></span>

### <span data-ttu-id="62ba7-109">Przykład 1 Pobierz wszystkie IotHub connectionStrings</span><span class="sxs-lookup"><span data-stu-id="62ba7-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="62ba7-110">Pobiera connectionStrings dla wszystkich kluczy iothub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="62ba7-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="62ba7-111">Przykład 2 uzyskiwanie connectionStrings IotHub dla określonego klucza</span><span class="sxs-lookup"><span data-stu-id="62ba7-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="62ba7-112">Pobiera connectionStrings dla klucza o nazwie "MyKey" dla iothub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="62ba7-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="62ba7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="62ba7-113">PARAMETERS</span></span>

### <span data-ttu-id="62ba7-114">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="62ba7-114">-KeyName</span></span>
<span data-ttu-id="62ba7-115">Nazwa klucza</span><span class="sxs-lookup"><span data-stu-id="62ba7-115">Name of the Key</span></span>

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

### <span data-ttu-id="62ba7-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="62ba7-116">-Name</span></span>
<span data-ttu-id="62ba7-117">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="62ba7-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="62ba7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62ba7-118">-ResourceGroupName</span></span>
<span data-ttu-id="62ba7-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="62ba7-119">Resource Group Name</span></span>

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

### <span data-ttu-id="62ba7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62ba7-120">-DefaultProfile</span></span>
<span data-ttu-id="62ba7-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="62ba7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62ba7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62ba7-122">CommonParameters</span></span>
<span data-ttu-id="62ba7-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62ba7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62ba7-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62ba7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62ba7-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62ba7-125">INPUTS</span></span>

### <span data-ttu-id="62ba7-126">System. String</span><span class="sxs-lookup"><span data-stu-id="62ba7-126">System.String</span></span>

## <span data-ttu-id="62ba7-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="62ba7-127">OUTPUTS</span></span>

### <span data-ttu-id="62ba7-128">Microsoft. Azure. Commands. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="62ba7-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="62ba7-129">System. Collections. Generic. list \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. MODELES. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral; PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="62ba7-129">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="62ba7-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="62ba7-130">NOTES</span></span>

## <span data-ttu-id="62ba7-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62ba7-131">RELATED LINKS</span></span>

