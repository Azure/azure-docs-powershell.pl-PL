---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 8546C3FE-5396-4027-BF33-F98F6C018A67
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorygatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
ms.openlocfilehash: d360a468d69306b5f203cbd28d17e9bfcc00bdcd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526894"
---
# <span data-ttu-id="3fe74-101">New-AzureRmDataFactoryGatewayKey</span><span class="sxs-lookup"><span data-stu-id="3fe74-101">New-AzureRmDataFactoryGatewayKey</span></span>

## <span data-ttu-id="3fe74-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3fe74-102">SYNOPSIS</span></span>
<span data-ttu-id="3fe74-103">Tworzy klucz bramy dla fabryki danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3fe74-103">Creates a gateway key for an Azure Data Factory.</span></span> <span data-ttu-id="3fe74-104">To polecenie cmdlet jest przestarzałe i zamiast tego powinno być używane polecenie **New-AzureRmDataFactoryGatewayAuthKey** .</span><span class="sxs-lookup"><span data-stu-id="3fe74-104">This cmdlet is deprecated, and you should use **New-AzureRmDataFactoryGatewayAuthKey** instead.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fe74-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3fe74-105">SYNTAX</span></span>

### <span data-ttu-id="3fe74-106">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3fe74-106">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGatewayKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fe74-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3fe74-107">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGatewayKey [-DataFactory] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fe74-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3fe74-108">DESCRIPTION</span></span>
<span data-ttu-id="3fe74-109">Polecenie cmdlet **New-AzureRmDataFactoryGatewayKey** tworzy klucz bramy dla określonej bramy usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="3fe74-109">The **New-AzureRmDataFactoryGatewayKey** cmdlet creates a gateway key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="3fe74-110">Użytkownik rejestruje bramę w usłudze chmury za pomocą tego klucza.</span><span class="sxs-lookup"><span data-stu-id="3fe74-110">You register the gateway with a cloud service by using this key.</span></span> <span data-ttu-id="3fe74-111">To polecenie cmdlet jest przestarzałe i zamiast tego powinno być używane polecenie **New-AzureRmDataFactoryGatewayAuthKey** .</span><span class="sxs-lookup"><span data-stu-id="3fe74-111">This cmdlet is deprecated, and you should use **New-AzureRmDataFactoryGatewayAuthKey** instead.</span></span>

## <span data-ttu-id="3fe74-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3fe74-112">EXAMPLES</span></span>

### <span data-ttu-id="3fe74-113">Przykład 1. Tworzenie klucza bramy</span><span class="sxs-lookup"><span data-stu-id="3fe74-113">Example 1: Create a gateway key</span></span>
```
PS C:\>New-AzureRmDataFactoryGatewayKey -ResourceGroupName "ADF" -GatewayName "ContosoGateway" -DataFactoryName "WikiADF" | Format-List
GatewayKey : ADF#40cbb3d9-2736-4794-a8a6-e6b839b4894f@a2d875ce-c9d7-4b8b-ad65-dd3ebbb9a940@8c0d1801-e863-44af-82e6-fb2f0c00f2ae@xz#Y9R0NhAeH3u7wgnrJyiWj4Y/QIhH4fFilIdzZgwsVQA=
```

<span data-ttu-id="3fe74-114">To polecenie tworzy klucz bramy dla bramy fabryki danych o nazwie ContosoGateway, a następnie przekazuje klucz bramy do polecenia cmdlet Format-List przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="3fe74-114">This command creates a gateway key for the data factory gateway named ContosoGateway, and then passes the gateway key to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3fe74-115">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="3fe74-115">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="3fe74-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3fe74-116">PARAMETERS</span></span>

### <span data-ttu-id="3fe74-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="3fe74-117">-DataFactory</span></span>
<span data-ttu-id="3fe74-118">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="3fe74-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="3fe74-119">To polecenie cmdlet tworzy klucz bramy dla fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="3fe74-119">This cmdlet creates a gateway key for the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fe74-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="3fe74-120">-DataFactoryName</span></span>
<span data-ttu-id="3fe74-121">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="3fe74-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="3fe74-122">To polecenie cmdlet tworzy klucz bramy dla fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="3fe74-122">This cmdlet creates a gateway key for the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fe74-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fe74-123">-DefaultProfile</span></span>
<span data-ttu-id="3fe74-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3fe74-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3fe74-125">-Bramaname</span><span class="sxs-lookup"><span data-stu-id="3fe74-125">-GatewayName</span></span>
<span data-ttu-id="3fe74-126">Określa nazwę bramy.</span><span class="sxs-lookup"><span data-stu-id="3fe74-126">Specifies the name of the gateway.</span></span>
<span data-ttu-id="3fe74-127">To polecenie cmdlet tworzy klucz dla bramy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="3fe74-127">This cmdlet creates a key for the gateway that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fe74-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fe74-128">-ResourceGroupName</span></span>
<span data-ttu-id="3fe74-129">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3fe74-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3fe74-130">To polecenie cmdlet tworzy klucz dla bramy należącej do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="3fe74-130">This cmdlet creates a key for a gateway that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fe74-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fe74-131">CommonParameters</span></span>
<span data-ttu-id="3fe74-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fe74-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fe74-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fe74-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fe74-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3fe74-134">INPUTS</span></span>

### <span data-ttu-id="3fe74-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3fe74-135">None</span></span>
<span data-ttu-id="3fe74-136">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3fe74-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3fe74-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3fe74-137">OUTPUTS</span></span>

### <span data-ttu-id="3fe74-138">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGatewayKey</span><span class="sxs-lookup"><span data-stu-id="3fe74-138">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGatewayKey</span></span>

## <span data-ttu-id="3fe74-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3fe74-139">NOTES</span></span>
* <span data-ttu-id="3fe74-140">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="3fe74-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3fe74-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3fe74-141">RELATED LINKS</span></span>

<span data-ttu-id="3fe74-142">[Nowe — AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md) 
 [Nowe — AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="3fe74-142">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)
[New-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span></span>


