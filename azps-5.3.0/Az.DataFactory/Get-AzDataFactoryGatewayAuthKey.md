---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 8e86597292a9bcfef2163100d273d1e27daeb32a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503700"
---
# <span data-ttu-id="fedb0-101">Get-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="fedb0-101">Get-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="fedb0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fedb0-102">SYNOPSIS</span></span>
<span data-ttu-id="fedb0-103">Pobiera klucz uwierzytelniania bramy dla fabryki danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fedb0-103">Gets gateway auth key for an Azure Data Factory.</span></span>

## <span data-ttu-id="fedb0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fedb0-104">SYNTAX</span></span>

### <span data-ttu-id="fedb0-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fedb0-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fedb0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fedb0-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fedb0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fedb0-107">DESCRIPTION</span></span>
<span data-ttu-id="fedb0-108">Polecenie cmdlet **Get-AzDataFactoryGatewayAuthKey** Pobiera klucz uwierzytelniania bramy dla określonej bramy usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="fedb0-108">The **Get-AzDataFactoryGatewayAuthKey** cmdlet gets gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="fedb0-109">Użytkownik rejestruje bramę w usłudze chmury, korzystając z tego KEY1 lub key2 tego klucza uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="fedb0-109">You register the gateway with a cloud service by using this key1 or key2 of this auth key.</span></span>

## <span data-ttu-id="fedb0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fedb0-110">EXAMPLES</span></span>

### <span data-ttu-id="fedb0-111">Przykład 1: Pobiera klucz uwierzytelniania bramy</span><span class="sxs-lookup"><span data-stu-id="fedb0-111">Example 1: Gets auth key of a gateway</span></span>
```
PS C:\> Get-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@ZgBjjX6GfJcrzTQInEV9PoOqsDrqOmC
       gGHqUg1THLqA=
Key2 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@kFXxBdFCEBeL7LPB3hA3LqLd1uNFbyv
       YmWxtV4WD3JQ=
```

<span data-ttu-id="fedb0-112">To polecenie pobiera klucz uwierzytelniania bramy dla bramy fabryki danych o nazwie Moja brama.</span><span class="sxs-lookup"><span data-stu-id="fedb0-112">This command gets gateway auth key for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="fedb0-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fedb0-113">PARAMETERS</span></span>

### <span data-ttu-id="fedb0-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="fedb0-114">-DataFactoryName</span></span>
<span data-ttu-id="fedb0-115">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="fedb0-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fedb0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fedb0-116">-DefaultProfile</span></span>
<span data-ttu-id="fedb0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fedb0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fedb0-118">-Bramaname</span><span class="sxs-lookup"><span data-stu-id="fedb0-118">-GatewayName</span></span>
<span data-ttu-id="fedb0-119">Nazwa bramy fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="fedb0-119">The data factory gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fedb0-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fedb0-120">-InputObject</span></span>
<span data-ttu-id="fedb0-121">Obiekt fabryki danych</span><span class="sxs-lookup"><span data-stu-id="fedb0-121">The data factory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: DataFactory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fedb0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fedb0-122">-ResourceGroupName</span></span>
<span data-ttu-id="fedb0-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fedb0-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fedb0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fedb0-124">CommonParameters</span></span>
<span data-ttu-id="fedb0-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fedb0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fedb0-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fedb0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fedb0-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fedb0-127">INPUTS</span></span>

### <span data-ttu-id="fedb0-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="fedb0-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="fedb0-129">System. String</span><span class="sxs-lookup"><span data-stu-id="fedb0-129">System.String</span></span>

## <span data-ttu-id="fedb0-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fedb0-130">OUTPUTS</span></span>

### <span data-ttu-id="fedb0-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="fedb0-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="fedb0-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fedb0-132">NOTES</span></span>
* <span data-ttu-id="fedb0-133">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="fedb0-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fedb0-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fedb0-134">RELATED LINKS</span></span>

<span data-ttu-id="fedb0-135">[Nowe — AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [Nowe — AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="fedb0-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span></span>

