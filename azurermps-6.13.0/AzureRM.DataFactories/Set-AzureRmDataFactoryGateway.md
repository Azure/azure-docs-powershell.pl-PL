---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryGateway.md
ms.openlocfilehash: c40999dfa9f1300502e8909a32eaf13a34d0bae0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548788"
---
# <span data-ttu-id="cdd51-101">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="cdd51-101">Set-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="cdd51-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cdd51-102">SYNOPSIS</span></span>
<span data-ttu-id="cdd51-103">Ustawia opis bramy w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="cdd51-103">Sets the description for a gateway in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdd51-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cdd51-104">SYNTAX</span></span>

### <span data-ttu-id="cdd51-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cdd51-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdd51-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cdd51-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdd51-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cdd51-107">DESCRIPTION</span></span>
<span data-ttu-id="cdd51-108">Polecenie cmdlet **Set-AzureRmDataFactoryGateway** ustawia opis określonej bramy w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="cdd51-108">The **Set-AzureRmDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="cdd51-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cdd51-109">EXAMPLES</span></span>

### <span data-ttu-id="cdd51-110">Przykład 1: Ustawianie opisu dla bramy</span><span class="sxs-lookup"><span data-stu-id="cdd51-110">Example 1: Set the description for a gateway</span></span>
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

<span data-ttu-id="cdd51-111">To polecenie ustawia opis bramy o nazwie ContosoGateway w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="cdd51-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="cdd51-112">Parametr Description określa nowy opis.</span><span class="sxs-lookup"><span data-stu-id="cdd51-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="cdd51-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cdd51-113">PARAMETERS</span></span>

### <span data-ttu-id="cdd51-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="cdd51-114">-DataFactory</span></span>
<span data-ttu-id="cdd51-115">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="cdd51-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="cdd51-116">To polecenie cmdlet ustawia opis bramy w fabryce danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cdd51-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdd51-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="cdd51-117">-DataFactoryName</span></span>
<span data-ttu-id="cdd51-118">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="cdd51-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="cdd51-119">To polecenie cmdlet ustawia opis bramy w fabryce danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cdd51-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cdd51-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdd51-120">-DefaultProfile</span></span>
<span data-ttu-id="cdd51-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cdd51-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cdd51-122">— Opis</span><span class="sxs-lookup"><span data-stu-id="cdd51-122">-Description</span></span>
<span data-ttu-id="cdd51-123">Określa opis bramy.</span><span class="sxs-lookup"><span data-stu-id="cdd51-123">Specifies a description for the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdd51-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cdd51-124">-Name</span></span>
<span data-ttu-id="cdd51-125">Określa nazwę bramy, dla której ma zostać ustawiony opis.</span><span class="sxs-lookup"><span data-stu-id="cdd51-125">Specifies the name of the gateway for which to set a description.</span></span>

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

### <span data-ttu-id="cdd51-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdd51-126">-ResourceGroupName</span></span>
<span data-ttu-id="cdd51-127">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cdd51-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="cdd51-128">To polecenie cmdlet ustawia opis bramy należącej do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="cdd51-128">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="cdd51-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdd51-129">CommonParameters</span></span>
<span data-ttu-id="cdd51-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdd51-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdd51-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdd51-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdd51-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cdd51-132">INPUTS</span></span>

### <span data-ttu-id="cdd51-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="cdd51-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="cdd51-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cdd51-134">System.String</span></span>

## <span data-ttu-id="cdd51-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cdd51-135">OUTPUTS</span></span>

### <span data-ttu-id="cdd51-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="cdd51-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="cdd51-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cdd51-137">NOTES</span></span>
* <span data-ttu-id="cdd51-138">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="cdd51-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="cdd51-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cdd51-139">RELATED LINKS</span></span>

[<span data-ttu-id="cdd51-140">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="cdd51-140">Get-AzureRmDataFactoryGateway</span></span>](./Get-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="cdd51-141">Nowe — AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="cdd51-141">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="cdd51-142">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="cdd51-142">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)


