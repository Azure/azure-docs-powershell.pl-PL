---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: ECF85C07-2C9E-487D-A2ED-77875C380244
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: af7184b3e43d2016ff4acc9e7634f831945a8fdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550764"
---
# <span data-ttu-id="6cdbf-101">Save-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="6cdbf-101">Save-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="6cdbf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6cdbf-102">SYNOPSIS</span></span>
<span data-ttu-id="6cdbf-103">Pobiera profil bramy zarządzania serwera i zapisuje go w pliku lokalnym.</span><span class="sxs-lookup"><span data-stu-id="6cdbf-103">Downloads the profile for a Server Management gateway and saves it to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cdbf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6cdbf-104">SYNTAX</span></span>

### <span data-ttu-id="6cdbf-105">ByName</span><span class="sxs-lookup"><span data-stu-id="6cdbf-105">ByName</span></span>
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-ResourceGroupName] <String>
 [-GatewayName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cdbf-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="6cdbf-106">ByObject</span></span>
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-Gateway] <Gateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cdbf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6cdbf-107">DESCRIPTION</span></span>
<span data-ttu-id="6cdbf-108">Polecenie cmdlet **Save-AzureRmServerManagementGatewayProfile** pobiera profil dla bramy zarządzania serwera Azure i zapisuje go w pliku lokalnym.</span><span class="sxs-lookup"><span data-stu-id="6cdbf-108">The **Save-AzureRmServerManagementGatewayProfile** cmdlet downloads the profile for an Azure Server Management gateway and stores it to a local file.</span></span>

## <span data-ttu-id="6cdbf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6cdbf-109">EXAMPLES</span></span>

## <span data-ttu-id="6cdbf-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6cdbf-110">PARAMETERS</span></span>

### <span data-ttu-id="6cdbf-111">-Gateway</span><span class="sxs-lookup"><span data-stu-id="6cdbf-111">-Gateway</span></span>
<span data-ttu-id="6cdbf-112">Określa bramę, dla której ten aplet polecenia pobiera profil.</span><span class="sxs-lookup"><span data-stu-id="6cdbf-112">Specifies the gateway that this cmdlet gets the profile for.</span></span>

<span data-ttu-id="6cdbf-113">Można użyć zamiast określania ResourceGroupName i Bramyname</span><span class="sxs-lookup"><span data-stu-id="6cdbf-113">May be used instead of specifying ResourceGroupName and GatewayName</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cdbf-114">-Bramaname</span><span class="sxs-lookup"><span data-stu-id="6cdbf-114">-GatewayName</span></span>
<span data-ttu-id="6cdbf-115">Określa nazwę bramy, dla której ten aplet polecenia pobiera profil.</span><span class="sxs-lookup"><span data-stu-id="6cdbf-115">Specifies the name of the gateway that this cmdlet gets the profile for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cdbf-116">-Plik_wyjściowy</span><span class="sxs-lookup"><span data-stu-id="6cdbf-116">-OutputFile</span></span>
<span data-ttu-id="6cdbf-117">Określa plik lokalny, w którym mają być zapisywane dane profilu.</span><span class="sxs-lookup"><span data-stu-id="6cdbf-117">Specifies the local file in which to save the profile data.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cdbf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cdbf-118">-ResourceGroupName</span></span>
<span data-ttu-id="6cdbf-119">Określa nazwę grupy zasobów, do której należy brama.</span><span class="sxs-lookup"><span data-stu-id="6cdbf-119">Specifies the name of the resource group that the gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cdbf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cdbf-120">-DefaultProfile</span></span>
<span data-ttu-id="6cdbf-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6cdbf-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cdbf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cdbf-122">CommonParameters</span></span>
<span data-ttu-id="6cdbf-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cdbf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cdbf-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cdbf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cdbf-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6cdbf-125">INPUTS</span></span>

### <span data-ttu-id="6cdbf-126">Problem</span><span class="sxs-lookup"><span data-stu-id="6cdbf-126">Gateway</span></span>
<span data-ttu-id="6cdbf-127">Parametr "brama" akceptuje wartość typu "brama" z procesu</span><span class="sxs-lookup"><span data-stu-id="6cdbf-127">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="6cdbf-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6cdbf-128">OUTPUTS</span></span>

### <span data-ttu-id="6cdbf-129">System. IO. FileInfo</span><span class="sxs-lookup"><span data-stu-id="6cdbf-129">System.IO.FileInfo</span></span>

## <span data-ttu-id="6cdbf-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6cdbf-130">NOTES</span></span>

## <span data-ttu-id="6cdbf-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6cdbf-131">RELATED LINKS</span></span>

[<span data-ttu-id="6cdbf-132">Zainstaluj — AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="6cdbf-132">Install-AzureRmServerManagementGatewayProfile</span></span>](./Install-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="6cdbf-133">Resetowanie — AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="6cdbf-133">Reset-AzureRmServerManagementGatewayProfile</span></span>](./Reset-AzureRmServerManagementGatewayProfile.md)


