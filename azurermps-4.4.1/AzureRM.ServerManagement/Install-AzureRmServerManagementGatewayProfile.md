---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 06081209-BBE5-4F76-86F8-9CF6197938F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: b1d3d757d7970a21a2d81af9f1e08d0d8126df96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717160"
---
# <span data-ttu-id="6114e-101">Install-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="6114e-101">Install-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="6114e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6114e-102">SYNOPSIS</span></span>
<span data-ttu-id="6114e-103">Instaluje profil bramy zarządzania serwera.</span><span class="sxs-lookup"><span data-stu-id="6114e-103">Installs a Server Management Gateway profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6114e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6114e-104">SYNTAX</span></span>

```
Install-AzureRmServerManagementGatewayProfile [[-InputFile] <FileInfo>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6114e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6114e-105">DESCRIPTION</span></span>
<span data-ttu-id="6114e-106">Polecenie cmdlet **Install-AzureRmServerManagementGatewayProfile** instaluje profil bramy usługi Azure Server Management Gateway w odpowiedniej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="6114e-106">The **Install-AzureRmServerManagementGatewayProfile** cmdlet installs an Azure Server Management Gateway profile into the correct location.</span></span>
<span data-ttu-id="6114e-107">Plik, który jest instalowany przez to polecenie cmdlet, nosi nazwę profile.jswłączony.</span><span class="sxs-lookup"><span data-stu-id="6114e-107">The file that this cmdlet installs is named profile.json.</span></span>

## <span data-ttu-id="6114e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6114e-108">EXAMPLES</span></span>

## <span data-ttu-id="6114e-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6114e-109">PARAMETERS</span></span>

### <span data-ttu-id="6114e-110">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="6114e-110">-InputFile</span></span>
<span data-ttu-id="6114e-111">Określa nazwę pliku lokalnego zawierającego profil bramy do zainstalowania.</span><span class="sxs-lookup"><span data-stu-id="6114e-111">Specifies the name of the local file that contains the gateway profile to install.</span></span>

<span data-ttu-id="6114e-112">Plik, który jest instalowany przez to polecenie cmdlet, powinien być wcześniej zapisany za pomocą polecenia cmdlet Save-AzureRmServerManagementGatewayProfile.</span><span class="sxs-lookup"><span data-stu-id="6114e-112">The file that this cmdlet installs should have been previously saved with the Save-AzureRmServerManagementGatewayProfile cmdlet.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6114e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6114e-113">-DefaultProfile</span></span>
<span data-ttu-id="6114e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6114e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6114e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6114e-115">CommonParameters</span></span>
<span data-ttu-id="6114e-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6114e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6114e-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6114e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6114e-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6114e-118">INPUTS</span></span>

### <span data-ttu-id="6114e-119">FileInfo</span><span class="sxs-lookup"><span data-stu-id="6114e-119">FileInfo</span></span>
<span data-ttu-id="6114e-120">Parametr "plik_wejściowy" przyjmuje wartość typu "FileInfo" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="6114e-120">Parameter 'InputFile' accepts value of type 'FileInfo' from the pipeline</span></span>

## <span data-ttu-id="6114e-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6114e-121">OUTPUTS</span></span>

## <span data-ttu-id="6114e-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6114e-122">NOTES</span></span>

## <span data-ttu-id="6114e-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6114e-123">RELATED LINKS</span></span>

[<span data-ttu-id="6114e-124">Resetowanie — AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="6114e-124">Reset-AzureRmServerManagementGatewayProfile</span></span>](./Reset-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="6114e-125">Zapisz — AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="6114e-125">Save-AzureRmServerManagementGatewayProfile</span></span>](./Save-AzureRmServerManagementGatewayProfile.md)


