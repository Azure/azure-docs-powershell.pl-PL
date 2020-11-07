---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: 1076ff16005665aa81e4775507a236fe62bb0965
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893114"
---
# <span data-ttu-id="e7f95-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="e7f95-101">Get-AzIotHub</span></span>

## <span data-ttu-id="e7f95-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e7f95-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f95-103">Pobiera informacje o IotHubs w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="e7f95-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="e7f95-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e7f95-104">SYNTAX</span></span>

### <span data-ttu-id="e7f95-105">ListIotHubsByResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e7f95-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7f95-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="e7f95-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7f95-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e7f95-107">DESCRIPTION</span></span>
<span data-ttu-id="e7f95-108">Pobiera informacje o IotHubs w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="e7f95-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="e7f95-109">Możesz wyświetlić wszystkie wystąpienia IotHub w ramach abonamentu lub filtrować wyniki według grupy zasobów lub określonej nazwy IotHub.</span><span class="sxs-lookup"><span data-stu-id="e7f95-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="e7f95-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e7f95-110">EXAMPLES</span></span>

### <span data-ttu-id="e7f95-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e7f95-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="e7f95-112">Pobiera wszystkie IotHubs z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e7f95-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="e7f95-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e7f95-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="e7f95-114">Pobiera wszystkie IotHubs z subskrypcji należącej do zasobu o nazwie "Moja zasobów".</span><span class="sxs-lookup"><span data-stu-id="e7f95-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="e7f95-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e7f95-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="e7f95-116">Pobiera informacje o IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="e7f95-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="e7f95-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e7f95-117">PARAMETERS</span></span>

### <span data-ttu-id="e7f95-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7f95-118">-DefaultProfile</span></span>
<span data-ttu-id="e7f95-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e7f95-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7f95-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e7f95-120">-Name</span></span>
<span data-ttu-id="e7f95-121">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="e7f95-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="e7f95-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7f95-122">-ResourceGroupName</span></span>
<span data-ttu-id="e7f95-123">Nazwa źródła danych</span><span class="sxs-lookup"><span data-stu-id="e7f95-123">Name of the ResourceGroup</span></span>

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

### <span data-ttu-id="e7f95-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f95-124">CommonParameters</span></span>
<span data-ttu-id="e7f95-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7f95-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f95-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7f95-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f95-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7f95-127">INPUTS</span></span>

### <span data-ttu-id="e7f95-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e7f95-128">System.String</span></span>

## <span data-ttu-id="e7f95-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e7f95-129">OUTPUTS</span></span>

### <span data-ttu-id="e7f95-130">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e7f95-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="e7f95-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e7f95-131">NOTES</span></span>

## <span data-ttu-id="e7f95-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7f95-132">RELATED LINKS</span></span>
