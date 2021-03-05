---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: ba5ab4214de0272338bac61cdf1bbabc9507a9ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988114"
---
# <span data-ttu-id="be2e9-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="be2e9-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="be2e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be2e9-102">SYNOPSIS</span></span>
<span data-ttu-id="be2e9-103">Pobiera połączenia z usługą IotHub.</span><span class="sxs-lookup"><span data-stu-id="be2e9-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="be2e9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="be2e9-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be2e9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="be2e9-105">DESCRIPTION</span></span>
<span data-ttu-id="be2e9-106">Pobiera połączenia z usługą IotHub.</span><span class="sxs-lookup"><span data-stu-id="be2e9-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="be2e9-107">Możesz uzyskać połączenia dla wszystkich kluczy lub przefiltrować je według określonej nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="be2e9-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="be2e9-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="be2e9-108">EXAMPLES</span></span>

### <span data-ttu-id="be2e9-109">Przykład 1. Pobierz wszystkie połączenia z usługą IotHub</span><span class="sxs-lookup"><span data-stu-id="be2e9-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="be2e9-110">Pobiera połączenia dla wszystkich kluczy dla usługi iothub o nazwie "myiothub"</span><span class="sxs-lookup"><span data-stu-id="be2e9-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="be2e9-111">Przykład 2. Uzyskiwanie połączeń połączeń aplikacji IotHub dla określonego klucza</span><span class="sxs-lookup"><span data-stu-id="be2e9-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="be2e9-112">Pobiera połączenia dla klucza o nazwie "mykey" dla aplikacji iothub o nazwie "myiothub"</span><span class="sxs-lookup"><span data-stu-id="be2e9-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="be2e9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be2e9-113">PARAMETERS</span></span>

### <span data-ttu-id="be2e9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be2e9-114">-DefaultProfile</span></span>
<span data-ttu-id="be2e9-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="be2e9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be2e9-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="be2e9-116">-KeyName</span></span>
<span data-ttu-id="be2e9-117">Nazwa klucza</span><span class="sxs-lookup"><span data-stu-id="be2e9-117">Name of the Key</span></span>

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

### <span data-ttu-id="be2e9-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="be2e9-118">-Name</span></span>
<span data-ttu-id="be2e9-119">Nazwa aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="be2e9-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="be2e9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be2e9-120">-ResourceGroupName</span></span>
<span data-ttu-id="be2e9-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="be2e9-121">Resource Group Name</span></span>

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

### <span data-ttu-id="be2e9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be2e9-122">CommonParameters</span></span>
<span data-ttu-id="be2e9-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be2e9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be2e9-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be2e9-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be2e9-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be2e9-125">INPUTS</span></span>

### <span data-ttu-id="be2e9-126">System.String</span><span class="sxs-lookup"><span data-stu-id="be2e9-126">System.String</span></span>

## <span data-ttu-id="be2e9-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be2e9-127">OUTPUTS</span></span>

### <span data-ttu-id="be2e9-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="be2e9-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="be2e9-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="be2e9-129">NOTES</span></span>

## <span data-ttu-id="be2e9-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be2e9-130">RELATED LINKS</span></span>
