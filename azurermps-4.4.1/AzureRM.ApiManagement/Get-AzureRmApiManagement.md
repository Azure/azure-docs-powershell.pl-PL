---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
ms.openlocfilehash: 610f8589dbb6c01cae1a3eb37f886425a3664929
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525813"
---
# <span data-ttu-id="3724c-101">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3724c-101">Get-AzureRmApiManagement</span></span>

## <span data-ttu-id="3724c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3724c-102">SYNOPSIS</span></span>
<span data-ttu-id="3724c-103">Pobiera listę lub określony Opis usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="3724c-103">Gets a list or a particular API Management Service description.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3724c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3724c-104">SYNTAX</span></span>

### <span data-ttu-id="3724c-105">Wszystkie w abonamentach (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="3724c-105">All In Subscription (Default)</span></span>
```
Get-AzureRmApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3724c-106">Cała grupa zasobów</span><span class="sxs-lookup"><span data-stu-id="3724c-106">All In Resource Group</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3724c-107">Określona usługa zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="3724c-107">Specific API Management Service</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3724c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3724c-108">DESCRIPTION</span></span>
<span data-ttu-id="3724c-109">Polecenie cmdlet **Get-AzureRmApiManagement** pobiera listę wszystkich usług zarządzania API w obszarze subskrypcja lub określona grupa zasobów lub w ramach określonego zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="3724c-109">The **Get-AzureRmApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="3724c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3724c-110">EXAMPLES</span></span>

### <span data-ttu-id="3724c-111">Przykład 1: uzyskiwanie wszystkich usług zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="3724c-111">Example 1: Get all API Management services</span></span>
```
PS C:\>Get-AzureRmApiManagement
```

<span data-ttu-id="3724c-112">To polecenie pobiera wszystkie usługi zarządzania API w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3724c-112">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="3724c-113">Przykład 2: uzyskiwanie wszystkich usług zarządzania interfejsem API według określonej nazwy</span><span class="sxs-lookup"><span data-stu-id="3724c-113">Example 2: Get all API Management services by a specific name</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="3724c-114">To polecenie pobiera całą usługę zarządzania interfejsem API według nazwy.</span><span class="sxs-lookup"><span data-stu-id="3724c-114">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="3724c-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3724c-115">PARAMETERS</span></span>

### <span data-ttu-id="3724c-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3724c-116">-Name</span></span>
<span data-ttu-id="3724c-117">Określa nazwę usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="3724c-117">Specifies the name of API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3724c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3724c-118">-ResourceGroupName</span></span>
<span data-ttu-id="3724c-119">Określa nazwę grupy zasobów, w której ten aplet polecenia pobiera usługę zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="3724c-119">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group, Specific API Management Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3724c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3724c-120">-DefaultProfile</span></span>
<span data-ttu-id="3724c-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3724c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3724c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3724c-122">CommonParameters</span></span>
<span data-ttu-id="3724c-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3724c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3724c-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3724c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3724c-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3724c-125">INPUTS</span></span>

## <span data-ttu-id="3724c-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3724c-126">OUTPUTS</span></span>

### <span data-ttu-id="3724c-127">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. ApiManagement. modele. PsApiManagement]</span><span class="sxs-lookup"><span data-stu-id="3724c-127">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement]</span></span>

## <span data-ttu-id="3724c-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3724c-128">NOTES</span></span>

## <span data-ttu-id="3724c-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3724c-129">RELATED LINKS</span></span>

[<span data-ttu-id="3724c-130">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3724c-130">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="3724c-131">Nowe — AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3724c-131">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="3724c-132">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3724c-132">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="3724c-133">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3724c-133">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


