---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: ac56d5392025a85d0310862a1786dde3d0f8ca2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868123"
---
# <span data-ttu-id="e4101-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="e4101-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="e4101-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4101-102">SYNOPSIS</span></span>
<span data-ttu-id="e4101-103">Pobiera klucz IotHub.</span><span class="sxs-lookup"><span data-stu-id="e4101-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="e4101-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4101-104">SYNTAX</span></span>

```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4101-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e4101-105">DESCRIPTION</span></span>
<span data-ttu-id="e4101-106">Pobiera klucz IotHub.</span><span class="sxs-lookup"><span data-stu-id="e4101-106">Gets an IotHub Key.</span></span>
<span data-ttu-id="e4101-107">Możesz wyświetlić listę wszystkich kluczy lub filtrować listę według określonej nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="e4101-107">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="e4101-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4101-108">EXAMPLES</span></span>

### <span data-ttu-id="e4101-109">Przykład 1 Pobierz wszystkie klucze</span><span class="sxs-lookup"><span data-stu-id="e4101-109">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="e4101-110">Pobiera wszystkie klucze IotHub o nazwie "myiothub"</span><span class="sxs-lookup"><span data-stu-id="e4101-110">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="e4101-111">Przykład 2 uzyskiwanie informacji dotyczących określonego klucza</span><span class="sxs-lookup"><span data-stu-id="e4101-111">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="e4101-112">Pobiera informacje dotyczące klucza o nazwie "iothubowner" dla IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="e4101-112">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="e4101-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4101-113">PARAMETERS</span></span>

### <span data-ttu-id="e4101-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4101-114">-DefaultProfile</span></span>
<span data-ttu-id="e4101-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e4101-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4101-116">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="e4101-116">-KeyName</span></span>
<span data-ttu-id="e4101-117">Nazwa klucza</span><span class="sxs-lookup"><span data-stu-id="e4101-117">Name of the Key</span></span>

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

### <span data-ttu-id="e4101-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e4101-118">-Name</span></span>
<span data-ttu-id="e4101-119">Nazwa Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="e4101-119">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="e4101-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4101-120">-ResourceGroupName</span></span>
<span data-ttu-id="e4101-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e4101-121">Resource Group Name</span></span>

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

### <span data-ttu-id="e4101-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4101-122">CommonParameters</span></span>
<span data-ttu-id="e4101-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4101-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4101-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4101-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4101-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4101-125">INPUTS</span></span>

### <span data-ttu-id="e4101-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e4101-126">System.String</span></span>

## <span data-ttu-id="e4101-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4101-127">OUTPUTS</span></span>

### <span data-ttu-id="e4101-128">Microsoft. Azure. Commands. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e4101-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="e4101-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4101-129">NOTES</span></span>

## <span data-ttu-id="e4101-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4101-130">RELATED LINKS</span></span>
