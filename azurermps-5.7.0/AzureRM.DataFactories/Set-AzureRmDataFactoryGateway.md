---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryGateway.md
ms.openlocfilehash: 5239f2143eefe40b777ad1077bbd26d6d645754c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526881"
---
# <span data-ttu-id="a02e5-101">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="a02e5-101">Set-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="a02e5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a02e5-102">SYNOPSIS</span></span>
<span data-ttu-id="a02e5-103">Ustawia opis bramy w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a02e5-103">Sets the description for a gateway in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a02e5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a02e5-104">SYNTAX</span></span>

### <span data-ttu-id="a02e5-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a02e5-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a02e5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a02e5-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a02e5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a02e5-107">DESCRIPTION</span></span>
<span data-ttu-id="a02e5-108">Polecenie cmdlet **Set-AzureRmDataFactoryGateway** ustawia opis określonej bramy w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a02e5-108">The **Set-AzureRmDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="a02e5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a02e5-109">EXAMPLES</span></span>

### <span data-ttu-id="a02e5-110">Przykład 1: Ustawianie opisu dla bramy</span><span class="sxs-lookup"><span data-stu-id="a02e5-110">Example 1: Set the description for a gateway</span></span>
```
PS C:\>Set-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
Name            : ContosoGateway
Description     : my gateway
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:31:09 AM
RegisterTime    : 8/22/2014 1:31:37 AM
LastConnectTime : 8/22/2014 1:41:41 AM
ExpiryTime      :
```

<span data-ttu-id="a02e5-111">To polecenie ustawia opis bramy o nazwie ContosoGateway w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="a02e5-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="a02e5-112">Parametr Description określa nowy opis.</span><span class="sxs-lookup"><span data-stu-id="a02e5-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="a02e5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a02e5-113">PARAMETERS</span></span>

### <span data-ttu-id="a02e5-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a02e5-114">-DataFactory</span></span>
<span data-ttu-id="a02e5-115">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="a02e5-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="a02e5-116">To polecenie cmdlet ustawia opis bramy w fabryce danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="a02e5-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a02e5-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="a02e5-117">-DataFactoryName</span></span>
<span data-ttu-id="a02e5-118">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="a02e5-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a02e5-119">To polecenie cmdlet ustawia opis bramy w fabryce danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="a02e5-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a02e5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a02e5-120">-DefaultProfile</span></span>
<span data-ttu-id="a02e5-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a02e5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a02e5-122">— Opis</span><span class="sxs-lookup"><span data-stu-id="a02e5-122">-Description</span></span>
<span data-ttu-id="a02e5-123">Określa opis bramy.</span><span class="sxs-lookup"><span data-stu-id="a02e5-123">Specifies a description for the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a02e5-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a02e5-124">-Name</span></span>
<span data-ttu-id="a02e5-125">Określa nazwę bramy, dla której ma zostać ustawiony opis.</span><span class="sxs-lookup"><span data-stu-id="a02e5-125">Specifies the name of the gateway for which to set a description.</span></span>

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

### <span data-ttu-id="a02e5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a02e5-126">-ResourceGroupName</span></span>
<span data-ttu-id="a02e5-127">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a02e5-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a02e5-128">To polecenie cmdlet ustawia opis bramy należącej do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="a02e5-128">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a02e5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a02e5-129">CommonParameters</span></span>
<span data-ttu-id="a02e5-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a02e5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a02e5-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a02e5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a02e5-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a02e5-132">INPUTS</span></span>

### <span data-ttu-id="a02e5-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a02e5-133">None</span></span>
<span data-ttu-id="a02e5-134">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="a02e5-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a02e5-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a02e5-135">OUTPUTS</span></span>

### <span data-ttu-id="a02e5-136">System. Collections. Generic. list "1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="a02e5-136">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span></span>

## <span data-ttu-id="a02e5-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a02e5-137">NOTES</span></span>
* <span data-ttu-id="a02e5-138">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="a02e5-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a02e5-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a02e5-139">RELATED LINKS</span></span>

[<span data-ttu-id="a02e5-140">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="a02e5-140">Get-AzureRmDataFactoryGateway</span></span>](./Get-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="a02e5-141">Nowe — AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="a02e5-141">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="a02e5-142">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="a02e5-142">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)


