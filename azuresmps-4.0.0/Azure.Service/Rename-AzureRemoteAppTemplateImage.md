---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 22571840-C27C-4208-A755-EF89E6C4B604
online version: ''
schema: 2.0.0
ms.openlocfilehash: 61cfeab9e02968c7b03e694b9913d4cbe4b3c90a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054440"
---
# <span data-ttu-id="b20ec-101">Rename-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="b20ec-101">Rename-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="b20ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b20ec-102">SYNOPSIS</span></span>
<span data-ttu-id="b20ec-103">Zmienia nazwę obrazu szablonu usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b20ec-103">Renames an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="b20ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b20ec-104">SYNTAX</span></span>

```
Rename-AzureRemoteAppTemplateImage [-ImageName] <String> [-NewName] <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b20ec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b20ec-105">DESCRIPTION</span></span>
<span data-ttu-id="b20ec-106">Polecenie cmdlet **Rename-AzureRemoteAppTemplateImage** umożliwia zmianę nazwy obrazu szablonu funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b20ec-106">The **Rename-AzureRemoteAppTemplateImage** cmdlet renames an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="b20ec-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b20ec-107">EXAMPLES</span></span>

### <span data-ttu-id="b20ec-108">Przykład 1: Zmienianie nazwy obrazu szablonu</span><span class="sxs-lookup"><span data-stu-id="b20ec-108">Example 1: Rename a template image</span></span>
```
PS C:\> Rename-AzureRemoteAppTemplateImage -ImageName "ContosoApps" -NewName "ContosoFinanceApps"
```

<span data-ttu-id="b20ec-109">To polecenie zmienia nazwę obrazu szablonu usługi Azure RemoteApp o nazwie ContosoApps na ContosoFinanceApps.</span><span class="sxs-lookup"><span data-stu-id="b20ec-109">This command renames the Azure RemoteApp template image named ContosoApps to ContosoFinanceApps.</span></span>

## <span data-ttu-id="b20ec-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b20ec-110">PARAMETERS</span></span>

### <span data-ttu-id="b20ec-111">-ImageName</span><span class="sxs-lookup"><span data-stu-id="b20ec-111">-ImageName</span></span>
<span data-ttu-id="b20ec-112">Określa nazwę obrazu szablonu usługi Azure RemoteApp, którego nazwę chcesz zmienić.</span><span class="sxs-lookup"><span data-stu-id="b20ec-112">Specifies the name of an Azure RemoteApp template image to rename.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b20ec-113">-NewName</span><span class="sxs-lookup"><span data-stu-id="b20ec-113">-NewName</span></span>
<span data-ttu-id="b20ec-114">Określa nową nazwę obrazu szablonu usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b20ec-114">Specifies a new name for an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20ec-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="b20ec-115">-Profile</span></span>
<span data-ttu-id="b20ec-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b20ec-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b20ec-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="b20ec-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20ec-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b20ec-118">CommonParameters</span></span>
<span data-ttu-id="b20ec-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b20ec-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b20ec-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b20ec-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b20ec-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b20ec-121">INPUTS</span></span>

## <span data-ttu-id="b20ec-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b20ec-122">OUTPUTS</span></span>

## <span data-ttu-id="b20ec-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b20ec-123">NOTES</span></span>

## <span data-ttu-id="b20ec-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b20ec-124">RELATED LINKS</span></span>

[<span data-ttu-id="b20ec-125">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="b20ec-125">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="b20ec-126">Nowe — AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="b20ec-126">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="b20ec-127">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="b20ec-127">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)


