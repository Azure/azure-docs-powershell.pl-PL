---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
ms.openlocfilehash: a1cb32d619a39b5b1a6fb1cd9c2c5eaa8dde55e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542587"
---
# <span data-ttu-id="4d13f-101">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="4d13f-101">Remove-AzureRmLogProfile</span></span>

## <span data-ttu-id="4d13f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d13f-102">SYNOPSIS</span></span>
<span data-ttu-id="4d13f-103">Usuwa profil dziennika.</span><span class="sxs-lookup"><span data-stu-id="4d13f-103">Removes a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d13f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d13f-104">SYNTAX</span></span>

```
Remove-AzureRmLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d13f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4d13f-105">DESCRIPTION</span></span>
<span data-ttu-id="4d13f-106">Polecenie cmdlet **Remove-AzureRmLogProfile** usuwa profil dziennika.</span><span class="sxs-lookup"><span data-stu-id="4d13f-106">The **Remove-AzureRmLogProfile** cmdlet removes a log profile.</span></span>

<span data-ttu-id="4d13f-107">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="4d13f-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="4d13f-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d13f-108">EXAMPLES</span></span>

## <span data-ttu-id="4d13f-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d13f-109">PARAMETERS</span></span>

### <span data-ttu-id="4d13f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d13f-110">-DefaultProfile</span></span>
<span data-ttu-id="4d13f-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4d13f-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d13f-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4d13f-112">-Name</span></span>
<span data-ttu-id="4d13f-113">Określa nazwę profilu dziennika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="4d13f-113">Specifies the name of the log profile to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d13f-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d13f-114">-PassThru</span></span>
<span data-ttu-id="4d13f-115">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4d13f-115">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d13f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d13f-116">CommonParameters</span></span>
<span data-ttu-id="4d13f-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d13f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d13f-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d13f-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d13f-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d13f-119">INPUTS</span></span>

### <span data-ttu-id="4d13f-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4d13f-120">None</span></span>
<span data-ttu-id="4d13f-121">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="4d13f-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4d13f-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d13f-122">OUTPUTS</span></span>

### <span data-ttu-id="4d13f-123">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4d13f-123">AzureOperationResponse</span></span>

## <span data-ttu-id="4d13f-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d13f-124">NOTES</span></span>

## <span data-ttu-id="4d13f-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d13f-125">RELATED LINKS</span></span>

[<span data-ttu-id="4d13f-126">Dodaj-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="4d13f-126">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="4d13f-127">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="4d13f-127">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)


