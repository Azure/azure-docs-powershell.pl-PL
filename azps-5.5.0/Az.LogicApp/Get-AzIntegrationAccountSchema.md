---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6C16B04B-459A-4B2C-B7DF-AC4D16FF7281
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
ms.openlocfilehash: ed85c1fea8bd338b3dd4f2a9e82ee5aac3f3b52b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194250"
---
# <span data-ttu-id="d4dd7-101">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="d4dd7-101">Get-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="d4dd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4dd7-102">SYNOPSIS</span></span>
<span data-ttu-id="d4dd7-103">Pobiera schematy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="d4dd7-103">Gets integration account schemas.</span></span>

## <span data-ttu-id="d4dd7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d4dd7-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountSchema [-ResourceGroupName <String>] [-Name <String>] [-SchemaName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4dd7-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d4dd7-105">DESCRIPTION</span></span>
<span data-ttu-id="d4dd7-106">Polecenie **cmdlet Get-AzIntegrationAccountSchema** pobiera schematy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="d4dd7-106">The **Get-AzIntegrationAccountSchema** cmdlet gets integration account schemas.</span></span>
<span data-ttu-id="d4dd7-107">Określanie nazwy konta integracji, nazwy grupy zasobów i nazwy schematu.</span><span class="sxs-lookup"><span data-stu-id="d4dd7-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="d4dd7-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="d4dd7-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d4dd7-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="d4dd7-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d4dd7-110">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="d4dd7-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d4dd7-111">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="d4dd7-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d4dd7-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d4dd7-112">EXAMPLES</span></span>

### <span data-ttu-id="d4dd7-113">Przykład 1. Uzyskiwanie schematu konta integracji</span><span class="sxs-lookup"><span data-stu-id="d4dd7-113">Example 1: Get an integration account schema</span></span>
```
PS C:\>Get-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
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

<span data-ttu-id="d4dd7-114">To polecenie pobiera schemat konta integracji o nazwie IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="d4dd7-114">This command gets the integration account schema named IntegrationAccountSchema43.</span></span>

### <span data-ttu-id="d4dd7-115">Przykład 2. Uzyskiwanie schematów konta integracji dla grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d4dd7-115">Example 2: Get integration account schemas for a resource group</span></span>
```
PS C:\>Get-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
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

<span data-ttu-id="d4dd7-116">To polecenie pobiera schematy kont integracji dla grupy zasobów o nazwie Grupa Zasobów11.</span><span class="sxs-lookup"><span data-stu-id="d4dd7-116">This command gets the integration account schemas for the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="d4dd7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4dd7-117">PARAMETERS</span></span>

### <span data-ttu-id="d4dd7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4dd7-118">-DefaultProfile</span></span>
<span data-ttu-id="d4dd7-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d4dd7-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4dd7-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d4dd7-120">-Name</span></span>
<span data-ttu-id="d4dd7-121">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="d4dd7-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="d4dd7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4dd7-122">-ResourceGroupName</span></span>
<span data-ttu-id="d4dd7-123">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d4dd7-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d4dd7-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="d4dd7-124">-SchemaName</span></span>
<span data-ttu-id="d4dd7-125">Określa nazwę schematu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="d4dd7-125">Specifies the name of an integration account schema.</span></span>
<span data-ttu-id="d4dd7-126">Określa nazwę schematu.</span><span class="sxs-lookup"><span data-stu-id="d4dd7-126">Specifies the name of a schema.</span></span>
<span data-ttu-id="d4dd7-127">.</span><span class="sxs-lookup"><span data-stu-id="d4dd7-127">.</span></span>

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

### <span data-ttu-id="d4dd7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4dd7-128">CommonParameters</span></span>
<span data-ttu-id="d4dd7-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4dd7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4dd7-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4dd7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4dd7-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4dd7-131">INPUTS</span></span>

### <span data-ttu-id="d4dd7-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d4dd7-132">System.String</span></span>

## <span data-ttu-id="d4dd7-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4dd7-133">OUTPUTS</span></span>

### <span data-ttu-id="d4dd7-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="d4dd7-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="d4dd7-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d4dd7-135">NOTES</span></span>

## <span data-ttu-id="d4dd7-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4dd7-136">RELATED LINKS</span></span>

[<span data-ttu-id="d4dd7-137">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="d4dd7-137">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="d4dd7-138">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="d4dd7-138">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="d4dd7-139">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="d4dd7-139">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


