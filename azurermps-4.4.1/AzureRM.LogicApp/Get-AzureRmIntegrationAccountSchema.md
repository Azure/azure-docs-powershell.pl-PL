---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 6C16B04B-459A-4B2C-B7DF-AC4D16FF7281
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: c34146079b419bceabfec1a2b9deb67c8eec658f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527489"
---
# <span data-ttu-id="8d96d-101">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="8d96d-101">Get-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="8d96d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8d96d-102">SYNOPSIS</span></span>
<span data-ttu-id="8d96d-103">Umożliwia pobieranie schematów kont integracji.</span><span class="sxs-lookup"><span data-stu-id="8d96d-103">Gets integration account schemas.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d96d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8d96d-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountSchema [-ResourceGroupName <String>] [-Name <String>] [-SchemaName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d96d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8d96d-105">DESCRIPTION</span></span>
<span data-ttu-id="8d96d-106">Polecenie cmdlet **Get-AzureRmIntegrationAccountSchema** pobiera schematy kont integracji.</span><span class="sxs-lookup"><span data-stu-id="8d96d-106">The **Get-AzureRmIntegrationAccountSchema** cmdlet gets integration account schemas.</span></span>
<span data-ttu-id="8d96d-107">Określanie nazwy konta integracji, nazwy grupy zasobów i nazwy schematu.</span><span class="sxs-lookup"><span data-stu-id="8d96d-107">Specifying the integration account name, resource group name, and schema name.</span></span>

<span data-ttu-id="8d96d-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="8d96d-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8d96d-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="8d96d-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8d96d-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="8d96d-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8d96d-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="8d96d-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8d96d-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8d96d-112">EXAMPLES</span></span>

### <span data-ttu-id="8d96d-113">Przykład 1: uzyskiwanie schematu konta integracji</span><span class="sxs-lookup"><span data-stu-id="8d96d-113">Example 1: Get an integration account schema</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name                 : IntegrationAccountSchema43
Type                 : Microsoft.Logic/integrationAccounts/schemas
CreatedTime          : 3/25/2016 5:42:58 PM
ChangedTime          : 3/25/2016 5:42:58 PM
SchemaType           : Xml
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts469af4f3cf4047b7ac3a08c87948ec5f/3839E_XML_INTEGRATIONACCOUNTSCHEMA43-5A86631F61F
                       14513AA1185A52C6B2874?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 7901
MetaData             :
```

<span data-ttu-id="8d96d-114">To polecenie umożliwia wyświetlenie schematu konta integracji o nazwie IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="8d96d-114">This command gets the integration account schema named IntegrationAccountSchema43.</span></span>

### <span data-ttu-id="8d96d-115">Przykład 2: pobieranie schematów kont integracji dla grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8d96d-115">Example 2: Get integration account schemas for a resource group</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name                 : IntegrationAccountSchema43
Type                 : Microsoft.Logic/integrationAccounts/schemas
CreatedTime          : 3/25/2016 5:42:58 PM
ChangedTime          : 3/25/2016 5:42:58 PM
SchemaType           : Xml
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts469af4f3cf4047b7ac3a08c87948ec5f/3839E_XML_INTEGRATIONACCOUNTSCHEMA43-5A86631F61F
                       14513AA1185A52C6B2874?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 7901
MetaData             :
```

<span data-ttu-id="8d96d-116">To polecenie pobiera schematy kont integracyjnych dla grupy zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8d96d-116">This command gets the integration account schemas for the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="8d96d-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8d96d-117">PARAMETERS</span></span>

### <span data-ttu-id="8d96d-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8d96d-118">-Name</span></span>
<span data-ttu-id="8d96d-119">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="8d96d-119">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d96d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d96d-120">-ResourceGroupName</span></span>
<span data-ttu-id="8d96d-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8d96d-121">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d96d-122">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="8d96d-122">-SchemaName</span></span>
<span data-ttu-id="8d96d-123">Określa nazwę schematu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="8d96d-123">Specifies the name of an integration account schema.</span></span>
<span data-ttu-id="8d96d-124">Określa nazwę schematu.</span><span class="sxs-lookup"><span data-stu-id="8d96d-124">Specifies the name of a schema.</span></span>
<span data-ttu-id="8d96d-125">.</span><span class="sxs-lookup"><span data-stu-id="8d96d-125">.</span></span>

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

### <span data-ttu-id="8d96d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d96d-126">-DefaultProfile</span></span>
<span data-ttu-id="8d96d-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8d96d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d96d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d96d-128">CommonParameters</span></span>
<span data-ttu-id="8d96d-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d96d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d96d-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d96d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d96d-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d96d-131">INPUTS</span></span>

## <span data-ttu-id="8d96d-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8d96d-132">OUTPUTS</span></span>

### <span data-ttu-id="8d96d-133">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="8d96d-133">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="8d96d-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8d96d-134">NOTES</span></span>

## <span data-ttu-id="8d96d-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d96d-135">RELATED LINKS</span></span>

[<span data-ttu-id="8d96d-136">Nowe — AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="8d96d-136">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="8d96d-137">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="8d96d-137">Remove-AzureRmIntegrationAccountSchema</span></span>](./Remove-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="8d96d-138">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="8d96d-138">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)


