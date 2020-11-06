---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/get-azurermlocationbasedservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccountKey.md
ms.openlocfilehash: 1f528bb0a80f039b9a2be7cb4cb6e4c7fbc740c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553664"
---
# <span data-ttu-id="cb9f7-101">Get-AzureRmLocationBasedServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="cb9f7-101">Get-AzureRmLocationBasedServicesAccountKey</span></span>

## <span data-ttu-id="cb9f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cb9f7-102">SYNOPSIS</span></span>
<span data-ttu-id="cb9f7-103">Pobiera klucze interfejsu API dla konta.</span><span class="sxs-lookup"><span data-stu-id="cb9f7-103">Gets the API keys for an account.</span></span> <span data-ttu-id="cb9f7-104">Klucze te są mechanizmem uwierzytelniania stosowanym w kolejnych połączeniach z usługami opartymi na lokalizacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cb9f7-104">These keys are the authentication mechanism used in subsequent calls to Azure Location Based Services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb9f7-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cb9f7-105">SYNTAX</span></span>

### <span data-ttu-id="cb9f7-106">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cb9f7-106">NameParameterSet (Default)</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb9f7-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb9f7-107">InputObjectParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb9f7-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb9f7-108">ResourceIdParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cb9f7-109">Opis</span><span class="sxs-lookup"><span data-stu-id="cb9f7-109">DESCRIPTION</span></span>
<span data-ttu-id="cb9f7-110">Polecenie cmdlet **Get-AzureRmLocationBasedServicesAccountKey** pobiera klucze interfejsu API dla konta usług opartego na zainicjowaniu obsługi lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="cb9f7-110">The **Get-AzureRmLocationBasedServicesAccountKey** cmdlet gets the API keys for a provisioned Location Based Services account.</span></span>

<span data-ttu-id="cb9f7-111">Konto usług opartych na lokalizacji ma dwa klucze API: podstawowy i pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="cb9f7-111">A Location Based Services account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="cb9f7-112">Klucze umożliwiają interakcję z punktem końcowym konta usługi opartego na lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="cb9f7-112">The keys enable interaction with the Location Based Services account endpoint.</span></span>

<span data-ttu-id="cb9f7-113">Użyj klawiszy [New-AzureRmLocationBasedServicesAccountKey](New-AzureRmLocationBasedServicesAccountKey.md) , aby ponownie wygenerować klucz.</span><span class="sxs-lookup"><span data-stu-id="cb9f7-113">Use [New-AzureRmLocationBasedServicesAccountKey](New-AzureRmLocationBasedServicesAccountKey.md) to regenerate a key.</span></span>

## <span data-ttu-id="cb9f7-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cb9f7-114">EXAMPLES</span></span>

### <span data-ttu-id="cb9f7-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cb9f7-115">Example 1</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="cb9f7-116">Zwraca klucze konta o nazwie Moje konto w grupie zasobu moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="cb9f7-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="cb9f7-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cb9f7-117">Example 2</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="cb9f7-118">Zwraca klucze określonego konta usług opartego na lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="cb9f7-118">Returns the keys for the specified Location Based Services Account.</span></span>

## <span data-ttu-id="cb9f7-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cb9f7-119">PARAMETERS</span></span>

### <span data-ttu-id="cb9f7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb9f7-120">-DefaultProfile</span></span>
<span data-ttu-id="cb9f7-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cb9f7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb9f7-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cb9f7-122">-InputObject</span></span>
<span data-ttu-id="cb9f7-123">Konto usług opartych na lokalizacji potoku w usłudze [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span><span class="sxs-lookup"><span data-stu-id="cb9f7-123">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

```yaml
Type: PSLocationBasedServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb9f7-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cb9f7-124">-Name</span></span>
<span data-ttu-id="cb9f7-125">Nazwa konta usług opartych na lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="cb9f7-125">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb9f7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb9f7-126">-ResourceGroupName</span></span>
<span data-ttu-id="cb9f7-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cb9f7-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb9f7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb9f7-128">-ResourceId</span></span>
<span data-ttu-id="cb9f7-129">Identyfikator ResourceId konta usług opartych na lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="cb9f7-129">Location Based Services Account ResourceId.</span></span>
```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb9f7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb9f7-130">CommonParameters</span></span>
<span data-ttu-id="cb9f7-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb9f7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb9f7-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb9f7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb9f7-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb9f7-133">INPUTS</span></span>

### <span data-ttu-id="cb9f7-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cb9f7-134">System.String</span></span>

## <span data-ttu-id="cb9f7-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cb9f7-135">OUTPUTS</span></span>

### <span data-ttu-id="cb9f7-136">Microsoft. Azure. Commands. LocationBasedServices. models. PSLocationBasedServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="cb9f7-136">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccountKeys</span></span>

### <span data-ttu-id="cb9f7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb9f7-137">CommonParameters</span></span>
<span data-ttu-id="cb9f7-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb9f7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb9f7-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb9f7-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb9f7-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cb9f7-140">NOTES</span></span>

## <span data-ttu-id="cb9f7-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cb9f7-141">RELATED LINKS</span></span>
