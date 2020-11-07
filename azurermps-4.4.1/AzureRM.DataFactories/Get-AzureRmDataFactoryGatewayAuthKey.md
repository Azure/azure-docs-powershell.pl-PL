---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 9de30d10b34cf666b040c1b25b84e4afeae63a10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553956"
---
# <span data-ttu-id="b6489-101">Get-AzureRmDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="b6489-101">Get-AzureRmDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="b6489-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6489-102">SYNOPSIS</span></span>
<span data-ttu-id="b6489-103">Pobiera klucz uwierzytelniania bramy dla fabryki danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b6489-103">Gets gateway auth key for an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6489-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6489-104">SYNTAX</span></span>

### <span data-ttu-id="b6489-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b6489-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6489-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b6489-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryGatewayAuthKey -InputObject <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6489-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b6489-107">DESCRIPTION</span></span>
<span data-ttu-id="b6489-108">Polecenie cmdlet **Get-AzureRmDataFactoryGatewayAuthKey** Pobiera klucz uwierzytelniania bramy dla określonej bramy usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b6489-108">The **Get-AzureRmDataFactoryGatewayAuthKey** cmdlet gets gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="b6489-109">Użytkownik rejestruje bramę w usłudze chmury, korzystając z tego KEY1 lub key2 tego klucza uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="b6489-109">You register the gateway with a cloud service by using this key1 or key2 of this auth key.</span></span>

## <span data-ttu-id="b6489-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6489-110">EXAMPLES</span></span>

### <span data-ttu-id="b6489-111">Przykład 1: Pobiera klucz uwierzytelniania bramy</span><span class="sxs-lookup"><span data-stu-id="b6489-111">Example 1: Gets auth key of a gateway</span></span>
```
PS C:\> Get-AzureRmDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@ZgBjjX6GfJcrzTQInEV9PoOqsDrqOmC
       gGHqUg1THLqA=
Key2 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@kFXxBdFCEBeL7LPB3hA3LqLd1uNFbyv
       YmWxtV4WD3JQ=
```

<span data-ttu-id="b6489-112">To polecenie pobiera klucz uwierzytelniania bramy dla bramy fabryki danych o nazwie Moja brama.</span><span class="sxs-lookup"><span data-stu-id="b6489-112">This command gets gateway auth key for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="b6489-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6489-113">PARAMETERS</span></span>

### <span data-ttu-id="b6489-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="b6489-114">-DataFactoryName</span></span>
<span data-ttu-id="b6489-115">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="b6489-115">The data factory name.</span></span>

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

### <span data-ttu-id="b6489-116">-Bramaname</span><span class="sxs-lookup"><span data-stu-id="b6489-116">-GatewayName</span></span>
<span data-ttu-id="b6489-117">Nazwa bramy fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="b6489-117">The data factory gateway name.</span></span>

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

### <span data-ttu-id="b6489-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6489-118">-ResourceGroupName</span></span>
<span data-ttu-id="b6489-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b6489-119">The resource group name.</span></span>

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

### <span data-ttu-id="b6489-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6489-120">-DefaultProfile</span></span>
<span data-ttu-id="b6489-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6489-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6489-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b6489-122">-InputObject</span></span>
<span data-ttu-id="b6489-123">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="b6489-123">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: DataFactory

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6489-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6489-124">CommonParameters</span></span>
<span data-ttu-id="b6489-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6489-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6489-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6489-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6489-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6489-127">INPUTS</span></span>

### <span data-ttu-id="b6489-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b6489-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>
<span data-ttu-id="b6489-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b6489-129">System.String</span></span>

## <span data-ttu-id="b6489-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6489-130">OUTPUTS</span></span>

### <span data-ttu-id="b6489-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="b6489-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="b6489-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6489-132">NOTES</span></span>
* <span data-ttu-id="b6489-133">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="b6489-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b6489-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6489-134">RELATED LINKS</span></span>

<span data-ttu-id="b6489-135">[Nowe — AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [Nowe — AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="b6489-135">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[New-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span></span>
