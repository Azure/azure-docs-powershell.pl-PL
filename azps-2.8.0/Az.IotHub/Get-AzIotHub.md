---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: d544de6badaa6ce64e8165696cc7dff2a595d75e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705253"
---
# <span data-ttu-id="4da2f-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="4da2f-101">Get-AzIotHub</span></span>

## <span data-ttu-id="4da2f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4da2f-102">SYNOPSIS</span></span>
<span data-ttu-id="4da2f-103">Pobiera informacje o IotHubs w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="4da2f-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="4da2f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4da2f-104">SYNTAX</span></span>

### <span data-ttu-id="4da2f-105">ListIotHubsByResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4da2f-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4da2f-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="4da2f-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4da2f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4da2f-107">DESCRIPTION</span></span>
<span data-ttu-id="4da2f-108">Pobiera informacje o IotHubs w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="4da2f-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="4da2f-109">Możesz wyświetlić wszystkie wystąpienia IotHub w ramach abonamentu lub filtrować wyniki według grupy zasobów lub określonej nazwy IotHub.</span><span class="sxs-lookup"><span data-stu-id="4da2f-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="4da2f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4da2f-110">EXAMPLES</span></span>

### <span data-ttu-id="4da2f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4da2f-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="4da2f-112">Pobiera wszystkie IotHubs z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="4da2f-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="4da2f-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4da2f-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="4da2f-114">Pobiera wszystkie IotHubs z subskrypcji należącej do zasobu o nazwie "Moja zasobów".</span><span class="sxs-lookup"><span data-stu-id="4da2f-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="4da2f-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="4da2f-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="4da2f-116">Pobiera informacje o IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="4da2f-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="4da2f-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4da2f-117">PARAMETERS</span></span>

### <span data-ttu-id="4da2f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4da2f-118">-DefaultProfile</span></span>
<span data-ttu-id="4da2f-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4da2f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4da2f-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4da2f-120">-Name</span></span>
<span data-ttu-id="4da2f-121">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="4da2f-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da2f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4da2f-122">-ResourceGroupName</span></span>
<span data-ttu-id="4da2f-123">Nazwa źródła danych</span><span class="sxs-lookup"><span data-stu-id="4da2f-123">Name of the ResourceGroup</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotHubsByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da2f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4da2f-124">CommonParameters</span></span>
<span data-ttu-id="4da2f-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4da2f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4da2f-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4da2f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4da2f-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4da2f-127">INPUTS</span></span>

### <span data-ttu-id="4da2f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4da2f-128">System.String</span></span>

## <span data-ttu-id="4da2f-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4da2f-129">OUTPUTS</span></span>

### <span data-ttu-id="4da2f-130">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4da2f-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="4da2f-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4da2f-131">NOTES</span></span>

## <span data-ttu-id="4da2f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4da2f-132">RELATED LINKS</span></span>