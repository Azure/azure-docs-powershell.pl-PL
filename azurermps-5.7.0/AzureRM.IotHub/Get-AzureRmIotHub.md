---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
ms.openlocfilehash: 80b629fe3d5ff5e028b73b22af95243849ecede7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717112"
---
# <span data-ttu-id="72f2e-101">Get-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="72f2e-101">Get-AzureRmIotHub</span></span>

## <span data-ttu-id="72f2e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="72f2e-102">SYNOPSIS</span></span>
<span data-ttu-id="72f2e-103">Pobiera informacje o IotHubs w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="72f2e-103">Gets information about the IotHubs in a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72f2e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="72f2e-104">SYNTAX</span></span>

### <span data-ttu-id="72f2e-105">ListIotHubsByResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="72f2e-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzureRmIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="72f2e-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="72f2e-106">GetIotHubByName</span></span>
```
Get-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="72f2e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="72f2e-107">DESCRIPTION</span></span>
<span data-ttu-id="72f2e-108">Pobiera informacje o IotHubs w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="72f2e-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="72f2e-109">Możesz wyświetlić wszystkie wystąpienia IotHub w ramach abonamentu lub filtrować wyniki według grupy zasobów lub określonej nazwy IotHub.</span><span class="sxs-lookup"><span data-stu-id="72f2e-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="72f2e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="72f2e-110">EXAMPLES</span></span>

### <span data-ttu-id="72f2e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="72f2e-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHub
```

<span data-ttu-id="72f2e-112">Pobiera wszystkie IotHubs z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="72f2e-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="72f2e-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="72f2e-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="72f2e-114">Pobiera wszystkie IotHubs z subskrypcji należącej do zasobu o nazwie "Moja zasobów".</span><span class="sxs-lookup"><span data-stu-id="72f2e-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="72f2e-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="72f2e-115">Example 3</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="72f2e-116">Pobiera informacje o IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="72f2e-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="72f2e-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72f2e-117">PARAMETERS</span></span>

### <span data-ttu-id="72f2e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72f2e-118">-DefaultProfile</span></span>
<span data-ttu-id="72f2e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="72f2e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72f2e-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="72f2e-120">-Name</span></span>
<span data-ttu-id="72f2e-121">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="72f2e-121">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: GetIotHubByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72f2e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72f2e-122">-ResourceGroupName</span></span>
<span data-ttu-id="72f2e-123">Nazwa źródła danych</span><span class="sxs-lookup"><span data-stu-id="72f2e-123">Name of the ResourceGroup</span></span>

```yaml
Type: String
Parameter Sets: ListIotHubsByResourceGroup
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetIotHubByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72f2e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72f2e-124">CommonParameters</span></span>
<span data-ttu-id="72f2e-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72f2e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72f2e-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72f2e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72f2e-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72f2e-127">INPUTS</span></span>

### <span data-ttu-id="72f2e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="72f2e-128">System.String</span></span>

## <span data-ttu-id="72f2e-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="72f2e-129">OUTPUTS</span></span>

### <span data-ttu-id="72f2e-130">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="72f2e-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="72f2e-131">System. Collections. Generic. list \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. MODELES. PSIotHub, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral; PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="72f2e-131">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="72f2e-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="72f2e-132">NOTES</span></span>

## <span data-ttu-id="72f2e-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72f2e-133">RELATED LINKS</span></span>

