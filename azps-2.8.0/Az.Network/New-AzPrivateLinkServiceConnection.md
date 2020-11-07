---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceConnection.md
ms.openlocfilehash: 8669eed6e34b2f03d4da8f1f6490a95e4762241d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871371"
---
# <span data-ttu-id="2cafa-101">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="2cafa-101">New-AzPrivateLinkServiceConnection</span></span>

## <span data-ttu-id="2cafa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2cafa-102">SYNOPSIS</span></span>
<span data-ttu-id="2cafa-103">Umożliwia utworzenie konfiguracji połączenia z usługą link Private.</span><span class="sxs-lookup"><span data-stu-id="2cafa-103">Creates a private link service connection configuration.</span></span>

## <span data-ttu-id="2cafa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2cafa-104">SYNTAX</span></span>

### <span data-ttu-id="2cafa-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2cafa-105">SetByResource (Default)</span></span>
```
New-AzPrivateLinkServiceConnection -Name <String> -PrivateLinkService <PSPrivateLinkService>
 [-GroupId <String[]>] [-RequestMessage <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2cafa-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2cafa-106">SetByResourceId</span></span>
```
New-AzPrivateLinkServiceConnection -Name <String> -PrivateLinkServiceId <String> [-GroupId <String[]>]
 [-RequestMessage <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cafa-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2cafa-107">DESCRIPTION</span></span>
<span data-ttu-id="2cafa-108">Polecenie cmdlet **New-AzPrivateLinkServiceConnection** umożliwia utworzenie konfiguracji połączenia z usługą link Private.</span><span class="sxs-lookup"><span data-stu-id="2cafa-108">**The New-AzPrivateLinkServiceConnection** cmdlet creates a private link service connection configuration.</span></span>

## <span data-ttu-id="2cafa-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2cafa-109">EXAMPLES</span></span>

### <span data-ttu-id="2cafa-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2cafa-110">Example 1</span></span>
```
New-AzPrivateLinkServiceConnection -Name MyPLSConnection -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
```

<span data-ttu-id="2cafa-111">W tym przykładzie przedstawiono tworzenie obiektu połączenia usługi linku prywatnego w pamięci do użycia podczas tworzenia prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="2cafa-111">This example create a private link service connection object in memory for using in creating private endpoint.</span></span>

## <span data-ttu-id="2cafa-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2cafa-112">PARAMETERS</span></span>

### <span data-ttu-id="2cafa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cafa-113">-DefaultProfile</span></span>
<span data-ttu-id="2cafa-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2cafa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cafa-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="2cafa-115">-GroupId</span></span>
<span data-ttu-id="2cafa-116">Lista identyfikatorów grup.</span><span class="sxs-lookup"><span data-stu-id="2cafa-116">The list of group id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cafa-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2cafa-117">-Name</span></span>
<span data-ttu-id="2cafa-118">Nazwa usługi linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="2cafa-118">The name of private link service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cafa-119">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2cafa-119">-PrivateLinkService</span></span>
<span data-ttu-id="2cafa-120">Usługa link prywatny.</span><span class="sxs-lookup"><span data-stu-id="2cafa-120">The private link service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cafa-121">-PrivateLinkServiceId</span><span class="sxs-lookup"><span data-stu-id="2cafa-121">-PrivateLinkServiceId</span></span>
<span data-ttu-id="2cafa-122">Identyfikator prywatnej usługi link.</span><span class="sxs-lookup"><span data-stu-id="2cafa-122">The id of private link service.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cafa-123">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="2cafa-123">-RequestMessage</span></span>
<span data-ttu-id="2cafa-124">Komunikat żądania.</span><span class="sxs-lookup"><span data-stu-id="2cafa-124">The request message.</span></span>

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

### <span data-ttu-id="2cafa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cafa-125">CommonParameters</span></span>
<span data-ttu-id="2cafa-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cafa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cafa-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2cafa-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cafa-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2cafa-128">INPUTS</span></span>

### <span data-ttu-id="2cafa-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2cafa-129">None</span></span>

## <span data-ttu-id="2cafa-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2cafa-130">OUTPUTS</span></span>

### <span data-ttu-id="2cafa-131">Microsoft. Azure. Commands. Network. models. PSPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="2cafa-131">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection</span></span>

## <span data-ttu-id="2cafa-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2cafa-132">NOTES</span></span>

## <span data-ttu-id="2cafa-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2cafa-133">RELATED LINKS</span></span>

[<span data-ttu-id="2cafa-134">Nowe — AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2cafa-134">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)