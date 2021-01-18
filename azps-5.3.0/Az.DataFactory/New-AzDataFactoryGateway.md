---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4DCF54BA-CFFA-4555-8CA3-66B98F704EFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
ms.openlocfilehash: a4c755ab3f68eab2821807e7df6b9e24fad0df9d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501577"
---
# <span data-ttu-id="98448-101">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="98448-101">New-AzDataFactoryGateway</span></span>

## <span data-ttu-id="98448-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98448-102">SYNOPSIS</span></span>
<span data-ttu-id="98448-103">Tworzy bramę dla fabryki danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="98448-103">Creates a gateway for an Azure Data Factory.</span></span>

## <span data-ttu-id="98448-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98448-104">SYNTAX</span></span>

### <span data-ttu-id="98448-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="98448-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [[-Description] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98448-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="98448-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [[-Description] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98448-107">Opis</span><span class="sxs-lookup"><span data-stu-id="98448-107">DESCRIPTION</span></span>
<span data-ttu-id="98448-108">Polecenie cmdlet **New-AzDataFactoryGateway** tworzy bramę w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="98448-108">The **New-AzDataFactoryGateway** cmdlet creates a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="98448-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98448-109">EXAMPLES</span></span>

### <span data-ttu-id="98448-110">Przykład 1: Tworzenie bramy</span><span class="sxs-lookup"><span data-stu-id="98448-110">Example 1: Create a gateway</span></span>
```
PS C:\>New-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
Name              : ContosoGateway
Description       : my gateway
Version           : 
Status            : NeedRegistration
VersionStatus     : None
CreateTime        : 8/22/2014 1:40:34 AM
RegisterTime      : 
LastConnectTime   : 
ExpiryTime        : 
ProvisioningState : Succeeded
Key               : ADF#40cbb3d9-2736-4794-a8a6-e6b839b4894f@a2d875ce-c9d7-4b8b-ad65-dd3ebbb9a940@8c0d1801-e863-44af-82e6-fb2f0c00f2ae@xz#Y9R0NhAeH3u7wgnrJyiWj4Y/QIhH4fFilIdzZgwsVQA=
```

<span data-ttu-id="98448-111">To polecenie tworzy bramę o nazwie ContosoGateway w fabryce danych o nazwie WikiADF w grupie zasobów o nazwie ADF.</span><span class="sxs-lookup"><span data-stu-id="98448-111">This command creates a gateway named ContosoGateway in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="98448-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98448-112">PARAMETERS</span></span>

### <span data-ttu-id="98448-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="98448-113">-DataFactory</span></span>
<span data-ttu-id="98448-114">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="98448-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="98448-115">To polecenie cmdlet tworzy bramę dla fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="98448-115">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="98448-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="98448-116">-DataFactoryName</span></span>
<span data-ttu-id="98448-117">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="98448-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="98448-118">To polecenie cmdlet tworzy bramę dla fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="98448-118">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="98448-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98448-119">-DefaultProfile</span></span>
<span data-ttu-id="98448-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="98448-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98448-121">— Opis</span><span class="sxs-lookup"><span data-stu-id="98448-121">-Description</span></span>
<span data-ttu-id="98448-122">Określa opis bramy.</span><span class="sxs-lookup"><span data-stu-id="98448-122">Specifies a description for the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98448-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="98448-123">-Name</span></span>
<span data-ttu-id="98448-124">Określa nazwę bramy do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="98448-124">Specifies the name of the gateway to create.</span></span>

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

### <span data-ttu-id="98448-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98448-125">-ResourceGroupName</span></span>
<span data-ttu-id="98448-126">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="98448-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="98448-127">To polecenie cmdlet umożliwia utworzenie bramy należącej do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="98448-127">This cmdlet creates a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="98448-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98448-128">CommonParameters</span></span>
<span data-ttu-id="98448-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98448-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98448-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98448-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98448-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98448-131">INPUTS</span></span>

### <span data-ttu-id="98448-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="98448-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="98448-133">System. String</span><span class="sxs-lookup"><span data-stu-id="98448-133">System.String</span></span>

## <span data-ttu-id="98448-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98448-134">OUTPUTS</span></span>

### <span data-ttu-id="98448-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="98448-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="98448-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98448-136">NOTES</span></span>
* <span data-ttu-id="98448-137">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="98448-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="98448-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98448-138">RELATED LINKS</span></span>

[<span data-ttu-id="98448-139">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="98448-139">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="98448-140">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="98448-140">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


