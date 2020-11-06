---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 4813EE2B-16C4-4716-B6DD-9447A0B46F3D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCallbackUrl.md
ms.openlocfilehash: 6cbb37eb211c766959f2513abe3bbe1554bfdb23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527518"
---
# <span data-ttu-id="c4cda-101">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="c4cda-101">Get-AzureRmIntegrationAccountCallbackUrl</span></span>

## <span data-ttu-id="c4cda-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c4cda-102">SYNOPSIS</span></span>
<span data-ttu-id="c4cda-103">Pobiera adres URL zwrotnego konta integracyjnego.</span><span class="sxs-lookup"><span data-stu-id="c4cda-103">Gets an integration account callback URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4cda-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c4cda-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountCallbackUrl -ResourceGroupName <String> -Name <String> [-NotAfter <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4cda-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c4cda-105">DESCRIPTION</span></span>
<span data-ttu-id="c4cda-106">Polecenie cmdlet **Get-AzureRmIntegrationAccountCallbackUrl** Pobiera adres URL wywołania zwrotnego konta integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c4cda-106">The **Get-AzureRmIntegrationAccountCallbackUrl** cmdlet gets an integration account callback URL from a resource group.</span></span>
<span data-ttu-id="c4cda-107">To polecenie cmdlet zwraca obiekt **CallbackUrl** reprezentujący adres URL wywołania zwrotnego konta integracji.</span><span class="sxs-lookup"><span data-stu-id="c4cda-107">This cmdlet returns a **CallbackUrl** object that represents the integration account callback URL.</span></span>
<span data-ttu-id="c4cda-108">Określ nazwę konta integracji i nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c4cda-108">Specify the integration account name and resource group name.</span></span>

<span data-ttu-id="c4cda-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="c4cda-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c4cda-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="c4cda-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c4cda-111">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="c4cda-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c4cda-112">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="c4cda-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c4cda-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c4cda-113">EXAMPLES</span></span>

### <span data-ttu-id="c4cda-114">Przykład 1: Uzyskaj adres URL połączenia zwrotnego konta integracji</span><span class="sxs-lookup"><span data-stu-id="c4cda-114">Example 1: Get an integration account callback URL</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -NotAfter "03/25/2016 18:23:22"
CallBackUrl : https://<baseurl>/integrationAccounts/8811f0155a364b5e9618ba28f7180601?api-version=2015-08-01-preview&se=2016-03
              -25T18%3A23%3A22.0000000Z&sp=%2F%2Fread&sv=1.0&sig=<value>
```

<span data-ttu-id="c4cda-115">To polecenie pobiera adres URL połączenia zwrotnego konta integracji.</span><span class="sxs-lookup"><span data-stu-id="c4cda-115">This command gets an integration account callback URL.</span></span>

## <span data-ttu-id="c4cda-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c4cda-116">PARAMETERS</span></span>

### <span data-ttu-id="c4cda-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c4cda-117">-Name</span></span>
<span data-ttu-id="c4cda-118">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="c4cda-118">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4cda-119">-NotAfter</span><span class="sxs-lookup"><span data-stu-id="c4cda-119">-NotAfter</span></span>
<span data-ttu-id="c4cda-120">Określa datę wygaśnięcia adresu URL wywołania zwrotnego.</span><span class="sxs-lookup"><span data-stu-id="c4cda-120">Specifies the expiry date for the callback URL.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4cda-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4cda-121">-ResourceGroupName</span></span>
<span data-ttu-id="c4cda-122">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c4cda-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4cda-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4cda-123">-DefaultProfile</span></span>
<span data-ttu-id="c4cda-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c4cda-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4cda-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4cda-125">CommonParameters</span></span>
<span data-ttu-id="c4cda-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4cda-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4cda-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4cda-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4cda-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4cda-128">INPUTS</span></span>

## <span data-ttu-id="c4cda-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c4cda-129">OUTPUTS</span></span>

### <span data-ttu-id="c4cda-130">Microsoft. Azure. Management. Logic. MODELES. CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="c4cda-130">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span></span>

## <span data-ttu-id="c4cda-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c4cda-131">NOTES</span></span>

## <span data-ttu-id="c4cda-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4cda-132">RELATED LINKS</span></span>

[<span data-ttu-id="c4cda-133">Get-AzureRmLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="c4cda-133">Get-AzureRmLogicAppTriggerCallbackUrl</span></span>](./Get-AzureRmLogicAppTriggerCallbackUrl.md)


