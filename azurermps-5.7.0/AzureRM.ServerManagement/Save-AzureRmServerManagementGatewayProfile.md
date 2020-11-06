---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: ECF85C07-2C9E-487D-A2ED-77875C380244
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/save-azurermservermanagementgatewayprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: 8dd9aeaaf987fba155ca80b0c8739d44c80945e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542295"
---
# <span data-ttu-id="e3044-101">Save-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="e3044-101">Save-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="e3044-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e3044-102">SYNOPSIS</span></span>
<span data-ttu-id="e3044-103">Pobiera profil bramy zarządzania serwera i zapisuje go w pliku lokalnym.</span><span class="sxs-lookup"><span data-stu-id="e3044-103">Downloads the profile for a Server Management gateway and saves it to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3044-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e3044-104">SYNTAX</span></span>

### <span data-ttu-id="e3044-105">ByName</span><span class="sxs-lookup"><span data-stu-id="e3044-105">ByName</span></span>
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-ResourceGroupName] <String>
 [-GatewayName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3044-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="e3044-106">ByObject</span></span>
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-Gateway] <Gateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3044-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e3044-107">DESCRIPTION</span></span>
<span data-ttu-id="e3044-108">Polecenie cmdlet **Save-AzureRmServerManagementGatewayProfile** pobiera profil dla bramy zarządzania serwera Azure i zapisuje go w pliku lokalnym.</span><span class="sxs-lookup"><span data-stu-id="e3044-108">The **Save-AzureRmServerManagementGatewayProfile** cmdlet downloads the profile for an Azure Server Management gateway and stores it to a local file.</span></span>

## <span data-ttu-id="e3044-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e3044-109">EXAMPLES</span></span>

## <span data-ttu-id="e3044-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3044-110">PARAMETERS</span></span>

### <span data-ttu-id="e3044-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3044-111">-DefaultProfile</span></span>
<span data-ttu-id="e3044-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e3044-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3044-113">-Gateway</span><span class="sxs-lookup"><span data-stu-id="e3044-113">-Gateway</span></span>
<span data-ttu-id="e3044-114">Określa bramę, dla której ten aplet polecenia pobiera profil.</span><span class="sxs-lookup"><span data-stu-id="e3044-114">Specifies the gateway that this cmdlet gets the profile for.</span></span>

<span data-ttu-id="e3044-115">Można użyć zamiast określania ResourceGroupName i Bramyname</span><span class="sxs-lookup"><span data-stu-id="e3044-115">May be used instead of specifying ResourceGroupName and GatewayName</span></span>

```yaml
Type: Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3044-116">-Bramaname</span><span class="sxs-lookup"><span data-stu-id="e3044-116">-GatewayName</span></span>
<span data-ttu-id="e3044-117">Określa nazwę bramy, dla której ten aplet polecenia pobiera profil.</span><span class="sxs-lookup"><span data-stu-id="e3044-117">Specifies the name of the gateway that this cmdlet gets the profile for.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3044-118">-Plik_wyjściowy</span><span class="sxs-lookup"><span data-stu-id="e3044-118">-OutputFile</span></span>
<span data-ttu-id="e3044-119">Określa plik lokalny, w którym mają być zapisywane dane profilu.</span><span class="sxs-lookup"><span data-stu-id="e3044-119">Specifies the local file in which to save the profile data.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3044-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3044-120">-ResourceGroupName</span></span>
<span data-ttu-id="e3044-121">Określa nazwę grupy zasobów, do której należy brama.</span><span class="sxs-lookup"><span data-stu-id="e3044-121">Specifies the name of the resource group that the gateway belongs to.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3044-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3044-122">CommonParameters</span></span>
<span data-ttu-id="e3044-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3044-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3044-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3044-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3044-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3044-125">INPUTS</span></span>

### <span data-ttu-id="e3044-126">Problem</span><span class="sxs-lookup"><span data-stu-id="e3044-126">Gateway</span></span>
<span data-ttu-id="e3044-127">Parametr "brama" akceptuje wartość typu "brama" z procesu</span><span class="sxs-lookup"><span data-stu-id="e3044-127">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="e3044-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e3044-128">OUTPUTS</span></span>

### <span data-ttu-id="e3044-129">System. IO. FileInfo</span><span class="sxs-lookup"><span data-stu-id="e3044-129">System.IO.FileInfo</span></span>

## <span data-ttu-id="e3044-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e3044-130">NOTES</span></span>

## <span data-ttu-id="e3044-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3044-131">RELATED LINKS</span></span>

[<span data-ttu-id="e3044-132">Zainstaluj — AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="e3044-132">Install-AzureRmServerManagementGatewayProfile</span></span>](./Install-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="e3044-133">Resetowanie — AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="e3044-133">Reset-AzureRmServerManagementGatewayProfile</span></span>](./Reset-AzureRmServerManagementGatewayProfile.md)


