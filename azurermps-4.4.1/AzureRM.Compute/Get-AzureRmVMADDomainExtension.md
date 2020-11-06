---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
ms.openlocfilehash: e4431b657c72a82f1316f5eb8b74f45fac0f04aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528253"
---
# <span data-ttu-id="af327-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="af327-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="af327-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="af327-102">SYNOPSIS</span></span>
<span data-ttu-id="af327-103">Pobiera informacje o rozszerzeniu domeny usługi AD.</span><span class="sxs-lookup"><span data-stu-id="af327-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af327-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="af327-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af327-105">Opis</span><span class="sxs-lookup"><span data-stu-id="af327-105">DESCRIPTION</span></span>
<span data-ttu-id="af327-106">Polecenie cmdlet **Get-AzureRmVMADDomainExtension** pobiera informacje o określonym rozszerzeniu domeny usługi Azure Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="af327-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="af327-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="af327-107">EXAMPLES</span></span>

## <span data-ttu-id="af327-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="af327-108">PARAMETERS</span></span>

### <span data-ttu-id="af327-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af327-109">-DefaultProfile</span></span>
<span data-ttu-id="af327-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="af327-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af327-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="af327-111">-Name</span></span>
<span data-ttu-id="af327-112">Określa nazwę rozszerzenia domeny.</span><span class="sxs-lookup"><span data-stu-id="af327-112">Specifies the name of the domain extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af327-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af327-113">-ResourceGroupName</span></span>
<span data-ttu-id="af327-114">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="af327-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="af327-115">-Status</span><span class="sxs-lookup"><span data-stu-id="af327-115">-Status</span></span>
<span data-ttu-id="af327-116">Wskazuje, że to polecenie cmdlet pobiera widok wystąpienia rozszerzenia domeny.</span><span class="sxs-lookup"><span data-stu-id="af327-116">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af327-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="af327-117">-VMName</span></span>
<span data-ttu-id="af327-118">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="af327-118">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af327-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af327-119">CommonParameters</span></span>
<span data-ttu-id="af327-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af327-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af327-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af327-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af327-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af327-122">INPUTS</span></span>

## <span data-ttu-id="af327-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="af327-123">OUTPUTS</span></span>

## <span data-ttu-id="af327-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="af327-124">NOTES</span></span>

## <span data-ttu-id="af327-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af327-125">RELATED LINKS</span></span>

[<span data-ttu-id="af327-126">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="af327-126">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


