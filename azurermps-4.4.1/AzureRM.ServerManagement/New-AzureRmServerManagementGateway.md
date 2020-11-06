---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: D7485CB9-AE12-445B-8984-3D21FCA0E82F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
ms.openlocfilehash: 9cb98b9671f43ddd7acbcc84e8473a12da00f405
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546027"
---
# <span data-ttu-id="c614e-101">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="c614e-101">New-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="c614e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c614e-102">SYNOPSIS</span></span>
<span data-ttu-id="c614e-103">Tworzy bramę zarządzania serwera.</span><span class="sxs-lookup"><span data-stu-id="c614e-103">Creates a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c614e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c614e-104">SYNTAX</span></span>

```
New-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 [-AutoUpgrade] [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c614e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c614e-105">DESCRIPTION</span></span>
<span data-ttu-id="c614e-106">Polecenie cmdlet **New-AzureRmServerManagementGateway** umożliwia utworzenie bramy zarządzania serwerem Azure.</span><span class="sxs-lookup"><span data-stu-id="c614e-106">The **New-AzureRmServerManagementGateway** cmdlet creates an Azure Server Management gateway.</span></span>

## <span data-ttu-id="c614e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c614e-107">EXAMPLES</span></span>

## <span data-ttu-id="c614e-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c614e-108">PARAMETERS</span></span>

### <span data-ttu-id="c614e-109">-Autouaktualnienie</span><span class="sxs-lookup"><span data-stu-id="c614e-109">-AutoUpgrade</span></span>
<span data-ttu-id="c614e-110">Wskazuje, że brama zostanie automatycznie uaktualniona po opublikowaniu nowej wersji.</span><span class="sxs-lookup"><span data-stu-id="c614e-110">Indicates that the gateway will auto upgrade itself when a new version is released.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c614e-111">-Bramaname</span><span class="sxs-lookup"><span data-stu-id="c614e-111">-GatewayName</span></span>
<span data-ttu-id="c614e-112">Określa nazwę bramy, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c614e-112">Specifies the name of the gateway that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c614e-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c614e-113">-Location</span></span>
<span data-ttu-id="c614e-114">Określa lokalizację, w której ma zostać utworzona brama.</span><span class="sxs-lookup"><span data-stu-id="c614e-114">Specifies the location in which to create the gateway.</span></span>

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

### <span data-ttu-id="c614e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c614e-115">-ResourceGroupName</span></span>
<span data-ttu-id="c614e-116">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy bramę.</span><span class="sxs-lookup"><span data-stu-id="c614e-116">Specifies the name of the resource group in which this cmdlet creates the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c614e-117">-Tagi</span><span class="sxs-lookup"><span data-stu-id="c614e-117">-Tags</span></span>
<span data-ttu-id="c614e-118">Określa znaczniki jako pary klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="c614e-118">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="c614e-119">Za pomocą znaczników można identyfikować bramę z innych zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c614e-119">You can use tags to identify a Gateway from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c614e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c614e-120">-DefaultProfile</span></span>
<span data-ttu-id="c614e-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c614e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c614e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c614e-122">CommonParameters</span></span>
<span data-ttu-id="c614e-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c614e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c614e-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c614e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c614e-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c614e-125">INPUTS</span></span>

## <span data-ttu-id="c614e-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c614e-126">OUTPUTS</span></span>

### <span data-ttu-id="c614e-127">Microsoft. Azure. Commands. ServerManagement. model. Gateway</span><span class="sxs-lookup"><span data-stu-id="c614e-127">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="c614e-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c614e-128">NOTES</span></span>

## <span data-ttu-id="c614e-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c614e-129">RELATED LINKS</span></span>

[<span data-ttu-id="c614e-130">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="c614e-130">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="c614e-131">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="c614e-131">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


