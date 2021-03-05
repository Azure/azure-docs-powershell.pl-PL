---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4813EE2B-16C4-4716-B6DD-9447A0B46F3D
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountcallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
ms.openlocfilehash: c23e8ca566db3a3b3c93dcdc7a4fc53fc85979c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960625"
---
# <span data-ttu-id="ab2e0-101">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="ab2e0-101">Get-AzIntegrationAccountCallbackUrl</span></span>

## <span data-ttu-id="ab2e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab2e0-102">SYNOPSIS</span></span>
<span data-ttu-id="ab2e0-103">Pobiera adres URL zwrotnego wywołania zwrotnego konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ab2e0-103">Gets an integration account callback URL.</span></span>

## <span data-ttu-id="ab2e0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ab2e0-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCallbackUrl -ResourceGroupName <String> -Name <String> [-NotAfter <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab2e0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ab2e0-105">DESCRIPTION</span></span>
<span data-ttu-id="ab2e0-106">Polecenie **cmdlet Get-AzIntegrationAccountCallbackUrl** pobiera adres URL zwrotnego konta integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ab2e0-106">The **Get-AzIntegrationAccountCallbackUrl** cmdlet gets an integration account callback URL from a resource group.</span></span>
<span data-ttu-id="ab2e0-107">To polecenie cmdlet zwraca obiekt **CallbackUrl** reprezentujący adres URL zwrotnego konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ab2e0-107">This cmdlet returns a **CallbackUrl** object that represents the integration account callback URL.</span></span>
<span data-ttu-id="ab2e0-108">Określ nazwę konta integracji i nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ab2e0-108">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="ab2e0-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="ab2e0-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ab2e0-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="ab2e0-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ab2e0-111">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="ab2e0-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ab2e0-112">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="ab2e0-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ab2e0-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ab2e0-113">EXAMPLES</span></span>

### <span data-ttu-id="ab2e0-114">Przykład 1. Uzyskiwanie adresu URL zwrotnego zwrotnego konta integracji</span><span class="sxs-lookup"><span data-stu-id="ab2e0-114">Example 1: Get an integration account callback URL</span></span>
```
PS C:\>Get-AzIntegrationAccountCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -NotAfter "03/25/2016 18:23:22"
CallBackUrl : https://<baseurl>/integrationAccounts/8811f0155a364b5e9618ba28f7180601?api-version=2015-08-01-preview&se=2016-03
              -25T18%3A23%3A22.0000000Z&sp=%2F%2Fread&sv=1.0&sig=<value>
```

<span data-ttu-id="ab2e0-115">To polecenie otrzymuje adres URL wywołania zwrotnego konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ab2e0-115">This command gets an integration account callback URL.</span></span>

## <span data-ttu-id="ab2e0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab2e0-116">PARAMETERS</span></span>

### <span data-ttu-id="ab2e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab2e0-117">-DefaultProfile</span></span>
<span data-ttu-id="ab2e0-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ab2e0-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab2e0-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ab2e0-119">-Name</span></span>
<span data-ttu-id="ab2e0-120">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ab2e0-120">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="ab2e0-121">-NotAfter</span><span class="sxs-lookup"><span data-stu-id="ab2e0-121">-NotAfter</span></span>
<span data-ttu-id="ab2e0-122">Określa datę wygaśnięcia adresu URL zwrotnego.</span><span class="sxs-lookup"><span data-stu-id="ab2e0-122">Specifies the expiry date for the callback URL.</span></span>

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

### <span data-ttu-id="ab2e0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab2e0-123">-ResourceGroupName</span></span>
<span data-ttu-id="ab2e0-124">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ab2e0-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ab2e0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab2e0-125">CommonParameters</span></span>
<span data-ttu-id="ab2e0-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab2e0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab2e0-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab2e0-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab2e0-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab2e0-128">INPUTS</span></span>

### <span data-ttu-id="ab2e0-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ab2e0-129">System.String</span></span>

## <span data-ttu-id="ab2e0-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab2e0-130">OUTPUTS</span></span>

### <span data-ttu-id="ab2e0-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="ab2e0-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span></span>

## <span data-ttu-id="ab2e0-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ab2e0-132">NOTES</span></span>

## <span data-ttu-id="ab2e0-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab2e0-133">RELATED LINKS</span></span>

[<span data-ttu-id="ab2e0-134">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="ab2e0-134">Get-AzLogicAppTriggerCallbackUrl</span></span>](./Get-AzLogicAppTriggerCallbackUrl.md)


