---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: 41f7b921cb1977d7410c511be224b7e24623597b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502526"
---
# <span data-ttu-id="f71b3-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f71b3-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="f71b3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f71b3-102">SYNOPSIS</span></span>
<span data-ttu-id="f71b3-103">Pobiera listę lub określony Opis usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="f71b3-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="f71b3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f71b3-104">SYNTAX</span></span>

### <span data-ttu-id="f71b3-105">GetBySubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f71b3-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f71b3-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f71b3-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f71b3-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="f71b3-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f71b3-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f71b3-108">ByResourceId</span></span>
```
Get-AzApiManagement -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f71b3-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f71b3-109">DESCRIPTION</span></span>
<span data-ttu-id="f71b3-110">Polecenie cmdlet **Get-AzApiManagement** pobiera listę wszystkich usług zarządzania API w obszarze subskrypcja lub określona grupa zasobów lub w ramach określonego zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="f71b3-110">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="f71b3-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f71b3-111">EXAMPLES</span></span>

### <span data-ttu-id="f71b3-112">Przykład 1: uzyskiwanie wszystkich usług zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="f71b3-112">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="f71b3-113">To polecenie pobiera wszystkie usługi zarządzania API w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f71b3-113">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="f71b3-114">Przykład 2: uzyskiwanie wszystkich usług zarządzania interfejsem API według określonej nazwy</span><span class="sxs-lookup"><span data-stu-id="f71b3-114">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="f71b3-115">To polecenie pobiera całą usługę zarządzania interfejsem API według nazwy.</span><span class="sxs-lookup"><span data-stu-id="f71b3-115">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="f71b3-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f71b3-116">PARAMETERS</span></span>

### <span data-ttu-id="f71b3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f71b3-117">-DefaultProfile</span></span>
<span data-ttu-id="f71b3-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f71b3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f71b3-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f71b3-119">-Name</span></span>
<span data-ttu-id="f71b3-120">Określa nazwę usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="f71b3-120">Specifies the name of API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f71b3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f71b3-121">-ResourceGroupName</span></span>
<span data-ttu-id="f71b3-122">Określa nazwę grupy zasobów, w której ten aplet polecenia pobiera usługę zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="f71b3-122">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup, GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f71b3-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f71b3-123">-ResourceId</span></span>
<span data-ttu-id="f71b3-124">Identyfikator zasobu ARM usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="f71b3-124">Arm ResourceId of the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f71b3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f71b3-125">CommonParameters</span></span>
<span data-ttu-id="f71b3-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f71b3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f71b3-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f71b3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f71b3-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f71b3-128">INPUTS</span></span>

### <span data-ttu-id="f71b3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f71b3-129">System.String</span></span>

## <span data-ttu-id="f71b3-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f71b3-130">OUTPUTS</span></span>

### <span data-ttu-id="f71b3-131">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="f71b3-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="f71b3-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f71b3-132">NOTES</span></span>

## <span data-ttu-id="f71b3-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f71b3-133">RELATED LINKS</span></span>

[<span data-ttu-id="f71b3-134">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f71b3-134">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="f71b3-135">Nowe — AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f71b3-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="f71b3-136">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f71b3-136">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="f71b3-137">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f71b3-137">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


