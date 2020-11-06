---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 06081209-BBE5-4F76-86F8-9CF6197938F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/install-azurermservermanagementgatewayprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: b9563e9b8b7afb7b980f0b3cd307c76fb9c6e8be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542315"
---
# <span data-ttu-id="6a2ab-101">Install-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="6a2ab-101">Install-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="6a2ab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6a2ab-102">SYNOPSIS</span></span>
<span data-ttu-id="6a2ab-103">Instaluje profil bramy zarządzania serwera.</span><span class="sxs-lookup"><span data-stu-id="6a2ab-103">Installs a Server Management Gateway profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a2ab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6a2ab-104">SYNTAX</span></span>

```
Install-AzureRmServerManagementGatewayProfile [[-InputFile] <FileInfo>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a2ab-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6a2ab-105">DESCRIPTION</span></span>
<span data-ttu-id="6a2ab-106">Polecenie cmdlet **Install-AzureRmServerManagementGatewayProfile** instaluje profil bramy usługi Azure Server Management Gateway w odpowiedniej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="6a2ab-106">The **Install-AzureRmServerManagementGatewayProfile** cmdlet installs an Azure Server Management Gateway profile into the correct location.</span></span>
<span data-ttu-id="6a2ab-107">Plik, który jest instalowany przez to polecenie cmdlet, nosi nazwę profile.jswłączony.</span><span class="sxs-lookup"><span data-stu-id="6a2ab-107">The file that this cmdlet installs is named profile.json.</span></span>

## <span data-ttu-id="6a2ab-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6a2ab-108">EXAMPLES</span></span>

## <span data-ttu-id="6a2ab-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a2ab-109">PARAMETERS</span></span>

### <span data-ttu-id="6a2ab-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a2ab-110">-DefaultProfile</span></span>
<span data-ttu-id="6a2ab-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a2ab-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a2ab-112">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="6a2ab-112">-InputFile</span></span>
<span data-ttu-id="6a2ab-113">Określa nazwę pliku lokalnego zawierającego profil bramy do zainstalowania.</span><span class="sxs-lookup"><span data-stu-id="6a2ab-113">Specifies the name of the local file that contains the gateway profile to install.</span></span>

<span data-ttu-id="6a2ab-114">Plik, który jest instalowany przez to polecenie cmdlet, powinien być wcześniej zapisany za pomocą polecenia cmdlet Save-AzureRmServerManagementGatewayProfile.</span><span class="sxs-lookup"><span data-stu-id="6a2ab-114">The file that this cmdlet installs should have been previously saved with the Save-AzureRmServerManagementGatewayProfile cmdlet.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a2ab-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a2ab-115">CommonParameters</span></span>
<span data-ttu-id="6a2ab-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a2ab-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a2ab-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a2ab-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a2ab-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a2ab-118">INPUTS</span></span>

### <span data-ttu-id="6a2ab-119">FileInfo</span><span class="sxs-lookup"><span data-stu-id="6a2ab-119">FileInfo</span></span>
<span data-ttu-id="6a2ab-120">Parametr "plik_wejściowy" przyjmuje wartość typu "FileInfo" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="6a2ab-120">Parameter 'InputFile' accepts value of type 'FileInfo' from the pipeline</span></span>

## <span data-ttu-id="6a2ab-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6a2ab-121">OUTPUTS</span></span>

## <span data-ttu-id="6a2ab-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6a2ab-122">NOTES</span></span>

## <span data-ttu-id="6a2ab-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a2ab-123">RELATED LINKS</span></span>

[<span data-ttu-id="6a2ab-124">Resetowanie — AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="6a2ab-124">Reset-AzureRmServerManagementGatewayProfile</span></span>](./Reset-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="6a2ab-125">Zapisz — AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="6a2ab-125">Save-AzureRmServerManagementGatewayProfile</span></span>](./Save-AzureRmServerManagementGatewayProfile.md)


