---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationAzureActiveDirectoryApp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
ms.openlocfilehash: 2d7a7d61d5a29113f9b0e40340ae6b13b599115f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705748"
---
# <span data-ttu-id="b4244-101">New-AzDataMigrationAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="b4244-101">New-AzDataMigrationAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="b4244-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b4244-102">SYNOPSIS</span></span>
<span data-ttu-id="b4244-103">Utwórz nową instancję dane aplikacji Azure pozycji Azure.</span><span class="sxs-lookup"><span data-stu-id="b4244-103">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="b4244-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b4244-104">SYNTAX</span></span>

```
New-AzDataMigrationAzureActiveDirectoryApp -ApplicationId <String> -AppKey <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4244-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b4244-105">DESCRIPTION</span></span>
<span data-ttu-id="b4244-106">Utwórz nową instancję dane aplikacji Azure pozycji Azure.</span><span class="sxs-lookup"><span data-stu-id="b4244-106">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="b4244-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b4244-107">EXAMPLES</span></span>

### <span data-ttu-id="b4244-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b4244-108">Example 1</span></span>
```powershell
PS C:\> $secpasswd = ConvertTo-SecureString "Your Secret Key Here" -AsPlainText -Force
C:\> New-AzDmsAadApp -ApplicationId "Your AppId/Service Principal ID here" -AppKey $secpasswd
```
<span data-ttu-id="b4244-109">Identyfikator użytkownika: "Identyfikator podmiotu zabezpieczeń AppId/Service ID w tym miejscu" AppKey: System. Security. SecureString dzierżawy: "Identyfikator dzierżawy"</span><span class="sxs-lookup"><span data-stu-id="b4244-109">ApplicationId : "Your AppId/Service Principal Id here" AppKey        : System.Security.SecureString TenantId      : "Tenant Id"</span></span>

## <span data-ttu-id="b4244-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b4244-110">PARAMETERS</span></span>

### <span data-ttu-id="b4244-111">-AppKey</span><span class="sxs-lookup"><span data-stu-id="b4244-111">-AppKey</span></span>
<span data-ttu-id="b4244-112">Klucz usługi Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="b4244-112">Azure Active Directory Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4244-113">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="b4244-113">-ApplicationId</span></span>
<span data-ttu-id="b4244-114">Identyfikator aplikacji usługi Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="b4244-114">Azure Active Directory Application Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4244-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4244-115">-DefaultProfile</span></span>
<span data-ttu-id="b4244-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4244-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4244-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4244-117">CommonParameters</span></span>
<span data-ttu-id="b4244-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4244-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b4244-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4244-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4244-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4244-120">INPUTS</span></span>

### <span data-ttu-id="b4244-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b4244-121">None</span></span>

## <span data-ttu-id="b4244-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b4244-122">OUTPUTS</span></span>

### <span data-ttu-id="b4244-123">Microsoft. Azure. Commands. datamigration. models. PSAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="b4244-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="b4244-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b4244-124">NOTES</span></span>

## <span data-ttu-id="b4244-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4244-125">RELATED LINKS</span></span>