---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: D7485CB9-AE12-445B-8984-3D21FCA0E82F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/new-azurermservermanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
ms.openlocfilehash: f73d53fc3031fc72be950547e5b9c2b93a9a0079
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716828"
---
# <span data-ttu-id="580df-101">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="580df-101">New-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="580df-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="580df-102">SYNOPSIS</span></span>
<span data-ttu-id="580df-103">Tworzy bramę zarządzania serwera.</span><span class="sxs-lookup"><span data-stu-id="580df-103">Creates a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="580df-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="580df-104">SYNTAX</span></span>

```
New-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 [-AutoUpgrade] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="580df-105">Opis</span><span class="sxs-lookup"><span data-stu-id="580df-105">DESCRIPTION</span></span>
<span data-ttu-id="580df-106">Polecenie cmdlet **New-AzureRmServerManagementGateway** umożliwia utworzenie bramy zarządzania serwerem Azure.</span><span class="sxs-lookup"><span data-stu-id="580df-106">The **New-AzureRmServerManagementGateway** cmdlet creates an Azure Server Management gateway.</span></span>

## <span data-ttu-id="580df-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="580df-107">EXAMPLES</span></span>

## <span data-ttu-id="580df-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="580df-108">PARAMETERS</span></span>

### <span data-ttu-id="580df-109">-Autouaktualnienie</span><span class="sxs-lookup"><span data-stu-id="580df-109">-AutoUpgrade</span></span>
<span data-ttu-id="580df-110">Wskazuje, że brama zostanie automatycznie uaktualniona po opublikowaniu nowej wersji.</span><span class="sxs-lookup"><span data-stu-id="580df-110">Indicates that the gateway will auto upgrade itself when a new version is released.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="580df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="580df-111">-DefaultProfile</span></span>
<span data-ttu-id="580df-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="580df-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="580df-113">-Bramaname</span><span class="sxs-lookup"><span data-stu-id="580df-113">-GatewayName</span></span>
<span data-ttu-id="580df-114">Określa nazwę bramy, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="580df-114">Specifies the name of the gateway that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="580df-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="580df-115">-Location</span></span>
<span data-ttu-id="580df-116">Określa lokalizację, w której ma zostać utworzona brama.</span><span class="sxs-lookup"><span data-stu-id="580df-116">Specifies the location in which to create the gateway.</span></span>

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

### <span data-ttu-id="580df-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="580df-117">-ResourceGroupName</span></span>
<span data-ttu-id="580df-118">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy bramę.</span><span class="sxs-lookup"><span data-stu-id="580df-118">Specifies the name of the resource group in which this cmdlet creates the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="580df-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="580df-119">-Tag</span></span>
<span data-ttu-id="580df-120">Pary klucz/wartość skojarzone z bramą.</span><span class="sxs-lookup"><span data-stu-id="580df-120">Key/value pairs associated with the gateway.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="580df-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="580df-121">CommonParameters</span></span>
<span data-ttu-id="580df-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="580df-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="580df-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="580df-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="580df-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="580df-124">INPUTS</span></span>

### <span data-ttu-id="580df-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="580df-125">None</span></span>
<span data-ttu-id="580df-126">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="580df-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="580df-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="580df-127">OUTPUTS</span></span>

### <span data-ttu-id="580df-128">Microsoft. Azure. Commands. ServerManagement. model. Gateway</span><span class="sxs-lookup"><span data-stu-id="580df-128">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="580df-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="580df-129">NOTES</span></span>

## <span data-ttu-id="580df-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="580df-130">RELATED LINKS</span></span>

[<span data-ttu-id="580df-131">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="580df-131">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="580df-132">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="580df-132">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


